# OOPS-group-assignment

class Pet:
    def __init__(self, Harriet):
        self.name = Harriet
        self.hunger = 0
        self.energy = 10
        self.happiness = 5
        self.tricks = []

    def eat(self):
        self.hunger = max(0, self.hunger - 3)
        self.happiness = min(10, self.happiness + 1)

    def sleep(self):
        self.energy = min(10, self.energy + 5)

    def play(self):
        self.energy = max(0, self.energy - 2)
        self.happiness = min(10, self.happiness + 2)
        self.hunger = min(10, self.hunger + 1)

    def get_status(self):
        print(f"name: {self.name}")
        print(f"Hunger: {self.hunger}")
        print(f"Energy: {self.energy}")
        print(f"Happiness: {self.happiness}")

    def train(self, trick):
        self.tricks.append(trick)
        self.happiness = min(10, self.happiness + 1)

    def show_tricks(self):
        print(f"{self.name}'s tricks: {', '.join(self.tricks) if self.tricks else 'None'}")
