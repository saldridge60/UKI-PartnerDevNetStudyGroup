# A python file that demonstrates how python parses the different data structures (JSON, XML, YAML) 

import yaml 
import json
import xml.etree.ElementTree as ET

def main():
    with open("user.yaml") as file:
        data = yaml.safe_load(file)
        #print(data)

    with open("user.json") as file:
        data = json.load(file)
        #print(data)

    with open("user.xml") as file:
        tree = ET.parse(file)
        root = tree.getroot()

        for child in root:
            print(child.tag)
        
        
if __name__ == "__main__":
    main()