# Mukhtar Ayazhan
### Contact information:
- **E-mail:** ayazhanmuhtar01@gmail.com
- **GitHub:** [ayazhm](https://github.com/ayazhm)
- **LinkedIn** [ayazhanmukhtar](https://www.linkedin.com/in/ayazhan-mukhtar-0b05a91bb/)

### Summary:
I am currently studying at university to get bachelor degree in Computer science. My goal in RS School is to maake a first step as a web-developer and become qualified specialist in this area. I choose web-development as it combines hard skills in analysis & coding with UX-UI design.

### Skills:
#### I am aquinted with basic concepts of the following languages: 
- Python
- C++
- Java

### Code example:
#### The following function implements Dijkstra Search
```
def UCSearch(start, goal, barrier):
    G = {}
    G[start] = 0
    expandedNodes = set()
    fringe = set([start])
    
    parent = {}

    while len(fringe) > 0:
        #Pick the node in the fringe with the lowest G score
        curNode = None # initialize the current node.
        curGscore = None # initialize the G score of current node

        for pos in fringe:
            if curNode is None or G[pos] < curGscore:
                curGscore = G[pos]
                curNode = pos
        fringe.remove(curNode)

        #Check if our robot has reached the goal
        if curNode == goal:
            #Retrace our path backward
            path = [curNode]
            while curNode in parent:
                curNode = parent[curNode]
                path.append(curNode)
            path.reverse()
            return path, expandedNodes, G[goal] #Done!

        if curNode != goal:
            expandedNodes.add(curNode)
            children = get_neighbors(curNode)
            for child in children:
                if child not in expandedNodes:
                    cost = move_cost(child, barrier)
                    if child in fringe:
                        temp = G[child]
                        if G[curNode] + cost < temp:
                            G[child] = G[curNode] + cost
                            parent[child] = curNode
                    if child not in fringe:
                        fringe.add(child)
                        G[child] = curGscore + cost
                        parent[child] = curNode

    raise RuntimeError("UCS failed to find a solution")
```
### Experience:
Working towards... )

### Education:
- **Bachelor degree,** Nazarbayev University, Astana
  - _2019-2024_
  - Computer science
- **CodeAcademy,** online
  - Course name: Introduction to HTML & CSS

### Languages:
- Kazakh (native speaker)
- Enlish (upper-intermediate)
  - Current education is studied in English
- Russian (advanced)
