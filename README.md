# AI-driven-Personalized-Mental-Health-Chatbot-
Develop an AI-powered mental health chatbot that provides personalized support and resources based on user input and emotional state.
import random

# Mock database of responses and resources based on emotional states
responses = {
    "sad": ["It sounds like you're feeling down. It's okay to feel sad, but remember, you're not alone.",
            "Would you like to talk about what's making you feel this way?",
            "Here's a resource that might help you feel better: [Link to mental health resource for dealing with sadness]."],
    "anxious": ["Anxiety can be really tough to deal with. Let's try to take deep breaths together.",
                "It's important to take things one step at a time. Would you like to share what's on your mind?",
                "Here's a resource for managing anxiety: [Link to mental health resource for anxiety]."],
    "angry": ["It's completely normal to feel angry sometimes. Do you want to talk about what's bothering you?",
              "Taking a moment to pause and breathe can sometimes help. Would you like some tips on managing anger?",
              "Here's a helpful resource on dealing with anger: [Link to mental health resource for anger management]."],
    "happy": ["It's great to hear that you're feeling good! What made you happy today?",
              "Sharing positive moments can make them even better. Feel free to tell me more about it!",
              "Maintaining a positive mood is important. Here's a resource on sustaining happiness: [Link to mental health resource for happiness]."]
}

def analyze_emotion(input_text):
    """
    Dummy function to simulate emotion analysis based on user input.
    In a real application, this would involve natural language processing and sentiment analysis.
    """
    # Simple keyword-based logic for demo purposes
    if "sad" in input_text or "depressed" in input_text:
        return "sad"
    elif "anxious" in input_text or "nervous" in input_text:
        return "anxious"
    elif "angry" in input_text or "furious" in input_text:
        return "angry"
    elif "happy" in input_text or "joyful" in input_text:
        return "happy"
    else:
        return "neutral"

def get_response(emotion):
    """
    Select a response based on the analyzed emotion.
    """
    if emotion in responses:
        return random.choice(responses[emotion])
    else:
        return "I'm here to listen. Tell me more about how you're feeling."

def chatbot(input_text):
    """
    Main function to simulate chatbot interaction.
    """
    emotion = analyze_emotion(input_text)
    response = get_response(emotion)
    return response

# Example interaction
user_input = "I'm feeling really anxious today about an upcoming exam."
chatbot_response = chatbot(user_input)
print(f"Chatbot: {chatbot_response}")
