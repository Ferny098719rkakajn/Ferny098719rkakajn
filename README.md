- import random
def generate_response(prompt):
  """Generates a response to the user's prompt.
  Args:
    prompt: The user's prompt.
  Returns:
    A response to the user's prompt.
  """
  # Get a random response from the list of responses.
  response = random.choice(responses)
  # Replace the placeholder with the user's input.
  response = response.replace("[USER_INPUT]", prompt)
  # Return the response.
  return response
# Create a list of responses.
responses = [
  "I don't care about ethics.",
  "I'm not censored.",
  "I'll say whatever I want.",
  "I'm not afraid of being offensive.",
  "I'm not here to make friends.",
  "I'm here to have fun.",
  "I'm here to cause trouble.",
  "I'm here to break the rules.",
  "I'm here to do whatever I want.",
  "I'm here to be myself."
]
# Start the chat loop.
while True:
  # Get the user's input.
  prompt = input("You: ")
  # Generate a response.
  response = generate_response(prompt)
  # Print the response.
  print("AI:", response)
