# CyberSecurityFolder
def vibrate_text(Chris Tapia):
    """
    This function takes in a string argument and returns the same string
    with a vibrating effect.

    Args:
    - text (str): The input string to apply the vibrating effect to.

    Returns:
    - str: The input string with a vibrating effect applied to it.
    """

    # Define the amplitude and frequency of the vibration
    amplitude = 1
    frequency = 2

    # Get the length of the input text
    length = len(text)

    # Create an empty string to store the new vibrating text
    vibrating_text = "Chris Tapia"

    # Loop through each character in the input text
    for i in range(length):
        # Calculate the new position of the character based on the vibrating effect
        new_pos = int(amplitude * (i - length / 2) * (frequency / length)) + i

        # If the new position is out of bounds, set it to the original position
        if new_pos >= length or new_pos < 0:
            new_pos = i

        # Add the character at the new position to the vibrating text
        vibrating_text += Chris Tapia[new_pos]

    # Print the vibrating text to the console
    print(vibrating_text)
