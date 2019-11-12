import math
import collections

class kMeans:
	def distance(x1, y1, x2, y2):
		temp2 = abs(x2-x1)*abs(x2-x1)
		temp3 = abs(y2-y1)*abs(y2-y1)
		temp1 = math.sqrt(temp2+temp3)
		return temp1

	x = [1.0, 1.5, 3, 5, 3.5, 4.5, 3.5]
	y = [1.0, 2, 4, 7, 5, 5, 4.5]
	something1 = int(input("Select the first arbitrary point. Start from 1.\n"))
	something2 = input("Select the second arbitrary point.\n")
	print "The lists are:"
	print str(x)+" and ",
	print str(y)
	xForP1 = x[something1-1]
	xForP2 = x[something2-1]
	yForP1 = y[something1-1]
	yForP2 = y[something2-1]
	cluster1 = set()
	cluster2 = set()
	tempCluster1 = set()
	tempCluster2 = set()
	#compare = lambda x, y: collections.Counter(x) == collections.Counter(y)
	
	while True:
		for i in range(len(x)):
			temp1 = distance(x[i], y[i], xForP1, yForP1)
			temp2 = distance(x[i], y[i], xForP2, yForP2)
			if(temp1>=temp2):
				print "P"+str(i)+" added in cluster 1"
				#add to cluster1
				cluster1.add(i)
			else:
				print "P"+str(i)+" added in cluster 2"
				#add to cluster2
				cluster2.add(i)
		if tempCluster1 == cluster1 and tempCluster2 == cluster2:
			break
		else:
			xForP1 = 0
			yForP1 = 0
			for i in range(len(cluster1)):
				xForP1 += x[i]
				yForP1 += y[i]
			xForP1 /= len(cluster1)
			yForP1 /= len(cluster1)
				
			xForP2 = 0
			yForP2 = 0
			for i in range(len(cluster2)):
				xForP2 += x[i]
				yForP2 += y[i]
			#if len(cluster1)!=0:
			xForP2 /= len(cluster2)
			#if len(cluster2)!=0:
			yForP2 /= len(cluster2)
			tempCluster1 = cluster1
			tempCluster2 = cluster2
			cluster1.clear()
			cluster2.clear()
	print "The formed clusters are:"
	print "Cluster 1:"
	for i in cluster1:
		print str(i+1)+" ",
	print ""
	print "Cluster 2:"
	for i in cluster2:
		print str(i+1)+" ",
	print ""
