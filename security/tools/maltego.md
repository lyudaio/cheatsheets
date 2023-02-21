# Maltego Cheatsheet

Maltego is a powerful OSINT (Open Source Intelligence) tool for collecting and analyzing information about a target organization or individual. It provides a visual interface for data mining and information gathering. This cheatsheet covers the basic concepts of Maltego and its key features.

## Installation

Maltego can be downloaded and installed from the official website: https://www.maltego.com/download/.

## Terminology

Here are some important terms to know before using Maltego:

| Term           | Description                                                                                 |
| -------------- | ------------------------------------------------------------------------------------------- |
| Entity         | A piece of information that represents a person, company, website, or any other data point. |
| Transform      | A script or API that can be used to query or modify data in Maltego.                        |
| Maltego Client | The GUI (Graphical User Interface) that displays and manipulates the data.                  |
| Maltego Server | The back-end component that stores and manages the data.                                    |

## Basic Usage

1. Launch Maltego.
2. Create a new graph.
3. Drag an entity from the palette onto the graph.
4. Right-click on the entity and select "Run Transform" to execute a transform on the entity.
5. Select a transform from the list and click "Run".
6. The output entities will be added to the graph.

## Transform Types

There are several types of transforms in Maltego:

| Type     | Description                                                                                |
| -------- | ------------------------------------------------------------------------------------------ |
| Standard | Queries a data source and returns a set of entities.                                       |
| Explore  | Queries a data source and returns a set of entities along with relationships between them. |
| Entity   | Modifies a single entity.                                                                  |
| Overlay  | Adds additional information to an entity.                                                  |

## Common Transforms

Here are some commonly used transforms in Maltego:

| Transform Name         | Description                                       | Input        | Output               |
| ---------------------- | ------------------------------------------------- | ------------ | -------------------- |
| DNS NSLookup           | Resolves the IP addresses of a domain name.       | Domain       | IPv4 Address         |
| Website to IP Address  | Resolves the IP address of a website.             | Website      | IPv4 Address         |
| Twitter User to Tweets | Returns the most recent tweets by a Twitter user. | Twitter User | Tweet                |
| Google Maps Search     | Searches Google Maps for a location.              | Search Query | Google Maps Location |

## Custom Transforms

You can create your own transforms in Maltego using Python or Java. Here are the basic steps:

1. Create a new transform in Maltego.
2. Write the code for the transform in Python or Java.
3. Deploy the transform to the Maltego server.
4. Test the transform in Maltego.

Here's an example of a simple Python transform:

```python
#!/usr/bin/env python

from MaltegoTransform import *

def main():
    mt = MaltegoTransform()
    mt.parseArguments(sys.argv)
    input_entity = mt.getArg()
    output_entity = mt.addEntity("maltego.IPv4Address", "192.168.1.1")
    mt.returnOutput()

if __name__ == "__main__":
    main()
```

This transform takes an input entity and adds an IPv4 address entity to the graph.

## Additional Resources

- Official documentation: https://docs.maltego.com/
- Maltego forum: https://www.maltego.com/community/forum/
- Maltego tutorials: https://www.maltego.com/learn/tutorials/
- Maltego transforms hub: https://www.maltego.com/transforms-hub/
