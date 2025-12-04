# Pseudocode — City Navigation System

## Dijkstra Shortest Path — Ahmad Karam

FUNCTION dijkstra(start, destination):
    CREATE distance_map
    FOR each node IN graph:
        distance_map[node] = INFINITY
    END FOR

    distance_map[start] = 0
    CREATE priority_queue
    INSERT (start, 0)

    WHILE priority_queue NOT empty:
        current, dist = priority_queue.popMin()

        IF current == destination:
            BREAK

        FOR each neighbor IN graph[current]:
            newDist = dist + weight(current, neighbor)

            IF newDist < distance_map[neighbor]:
                distance_map[neighbor] = newDist
                parent[neighbor] = current
                priority_queue.insert(neighbor, newDist)
            END IF
        END FOR
    END WHILE

    RETURN constructPath(parent, destination)
END FUNCTION

