class Message:
    def __init__(self, content):
        self.content = content
        self.reactions = {}

    def add_reaction(self, user, emoji):
        if user in self.reactions:
            print(f"{user} changed their reaction to {emoji}.")
        else:
            print(f"{user} reacted with {emoji}.")
        self.reactions[user] = emoji

    def remove_reaction(self, user):
        if user in self.reactions:
            removed_emoji = self.reactions.pop(user)
            print(f"{user} removed their reaction {removed_emoji}.")
        else:
            print(f"{user} hasn't reacted yet.")

    def show_reactions(self):
        if not self.reactions:
            print("No reactions yet.")
        else:
            print("Reactions:")
            for user, emoji in self.reactions.items():
                print(f"{user}: {emoji}")


# Simulate WhatsApp-like reactions
def main():
    # List of emojis users can react with
    emoji_options = ['❤️', '😂', '😮', '😢', '👍', '👎']

    # Create a new message
    message = Message("Hey! How are you doing?")

    while True:
        print("\nMessage: ", message.content)
        print("\nAvailable reactions:", ', '.join(emoji_options))
        print("Options: (1) Add/Change reaction (2) Remove reaction (3) Show all reactions (4) Exit")

        choice = input("Select an option: ")

        if choice == '1':
            user = input("Enter your name: ")
            emoji = input(f"Select an emoji to react with {emoji_options}: ")
            if emoji in emoji_options:
                message.add_reaction(user, emoji)
            else:
                print("Invalid emoji! Try again.")
        elif choice == '2':
            user = input("Enter your name: ")
            message.remove_reaction(user)
        elif choice == '3':
            message.show_reactions()
        elif choice == '4':
            break
        else:
            print("Invalid choice! Try again.")


if __name__ == "__main__":
    main()
