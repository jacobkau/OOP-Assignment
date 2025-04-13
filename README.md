# OOP-Assignment completed
#Activity 1
#i
class Smartphone:
    def __init__(self, brand, model, properties):
        self.brand = brand
        self.model = model
        self.properties = properties
        
    def specs(self):
        return f"{self.brand} {self.model} {self.properties} is a powerful smartphone."

#ii
class GamingPhone(Smartphone):
    def __init__(self, brand, model,properties, gpu):
        super().__init__(brand,properties, model)
        self.__gpu = gpu  # Encapsulated attribute
        
    def specs(self):
        return f"{self.brand} {self.model} {self.properties} has a high-end GPU: {self.__gpu}."

#Activity 2
class Animal:
    def move(self):
        pass
class snake(Animal):
    def move(self):
        return "crawling"
class Bird(Animal):
    def move(self):
        return "Flying"
class frog(Animal):
    def move(self):
        return "jumping"
# Testing polymorphism
animals = [snake(), Bird(), frog()]
for a in animals:
    print(a.move())
