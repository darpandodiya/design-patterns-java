# Design Patterns for Humans™ - Java Implementation #

I wanted to strengthen my foundation of Design Patterns. I found one interesting guide on Reddit: [Design Patterns for Humans™ - An ultra-simplified explanation](https://github.com/kamranahmedse/design-patterns-for-humans "Design Patterns for Humans")

The guide reminded me of the "Head First" series books. Placid and easy to understand.

The examples given there were in PHP-7 so I wondered why not implement them in Java. And hence this repo.

Being in professional software engineering field since last couple of years, I've come across below patterns one or another time. Some patterns I've used unknowingly. Nevertheless, it's always great to have sound fundamentals. 

----------
## Types of Design Patterns ##
- Creational
- Structural
- Behavioral

## Creational Design Patterns ##
- Simple Factory
- Factory Method
- Abstract Factory
- Builder
- Prototype
- Singleton

## Structural Design Patterns ##
- Adapter
- Bridge
- Composite
- Decorator
- Facade
- Flyweight
- Proxy

## Behavioral Design Patterns ##
- Chain of Responsibility
- Command
- Iterator
- Mediator
- Memento
- Observer
- Visitor
- Strategy
- State
- Template Method

## Creational Design Pattern Examples ##

### Simple Factory ###
Simple factory simply generates an instance for client without exposing any instantiation logic to the client

**Code**

    interface Door {
		public float getWidth();
		public float getHeight();
	}

	class WoodenDoor implements Door {
		private float width;
		private float height;

		public WoodenDoor(float width, float height) {
			this.width = width;
			this.height = height;
		}

		public float getWidth() {
			return width;
		}

		public float getHeight() {
			return height;
		}	
	}

	class DoorFactory {
		public static Door makeDoor(float width, float height) {
			return new WoodenDoor(width, height);
		}
	}

	Usage:
	Door myDoor = DoorFactory.makeDoor(100, 200);
	Sysout("Width: " + myDoor.getWidth());
	Sysout("Height: " + myDoor.getHeight());

	

		


