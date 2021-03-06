# Video Query Home

Software for agile example-driven search of video datasets. 

_**How it works:**_ The user provides an example of a
video clip of interest, and the software searches for and returns examples of similar clips. 
The user then gives feedback
on which results match the user's intended search goal. Based on the user's feedback, the software performs another 
round of search. After a reasonable number of rounds, the design intent is for the software to be able to 
query the entire dataset for all matching clips and achieve a high degree of accuracy. 

The collaborative search approach
is more agile than conventional supervised learning of video actions.  It does not require an upfront specification
of the actions of interest, nor a large upfront investment in labeling data. The collaborative search can also help a user discern what aspects of the video clips
are important to match, since the user can experiment while giving feedback. 

_**[Example: Click here](https://github.com/PARC-projects/video-query-home/wiki/Web-Client-Example#example)**_

_**Overview of Project:**_ The front end is an Angular 6.x web application. It calls the RESTful Video Query API, 
which uses Video Query Algorithms to perform deep learning calculations. 
The API can also be used independently of the front end. 

![image](high-level-architecture.png)

_**Brief description of search algorithm:**_  The search algorithm uses embedded features from an ensemble of deep neural
networks pre-trained on UCF-101 data using the Temporal Segment Networks approach (1). Similiarities of clips
are quantified by computing dot products of embedded feature vectors for the example clips and possible matches. 
For a more detailed description of the Video Query algorithms, please see the reference [TBD arxiv pdf](https://arxiv.org/).

(1) Wang, Limin, Yuanjun Xiong, Zhe Wang, Yu Qiao, Dahua Lin, Xiaoou Tang, and Luc Van Gool. 
"Temporal segment networks: Towards good practices for deep action recognition." 
In European Conference on Computer Vision, pp. 20-36. Springer, Cham, 2016.

_**Acknowledgement:**_ This project was funded in part by the US Department of Transportation Federal Highway Administration
Exploratory Advanced Research Award DTFH6115H00006, with cost sharing by the Palo Alto Research Center.

## Getting Started

To get started, clone the repositories for the front end, API, and algorithms servers. 
Then go to the [Wiki](#wiki) for detailed instruction.

- [Video Query Client](https://github.com/PARC-projects/video-query-client-web)
- [Video Query API](https://github.com/PARC-projects/video-query-api)
- [Video Query Algorithms](https://github.com/PARC-projects/video-query-algorithms)

## Wiki

For detailed instruction on how to utilize this project, please have a look at our Wiki

- [Home](https://github.com/PARC-projects/video-query-home/wiki/Home)
- [Web Client](https://github.com/PARC-projects/video-query-home/wiki/Web-Client)
  - [Setup](https://github.com/PARC-projects/video-query-home/wiki/Web-Client-Setup)
  - [Example](https://github.com/PARC-projects/video-query-home/wiki/Web-Client-Example)
- [API](https://github.com/PARC-projects/video-query-home/wiki/Api)
  - [Setup](https://github.com/PARC-projects/video-query-home/wiki/Api-Setup)
  - [Database](https://github.com/PARC-projects/video-query-home/wiki/Api-Database)
  - [Tests](https://github.com/PARC-projects/video-query-home/wiki/Api-Tests)
- [Algorithms](https://github.com/PARC-projects/video-query-home/wiki/Algorithms)
  - [Pipeline](https://github.com/PARC-projects/video-query-home/wiki/Algorithms-Pipeline)
  - [Compute video features](https://github.com/PARC-projects/video-query-home/wiki/Algorithms-Compute-Video-Features)
  - [Database](https://github.com/PARC-projects/video-query-home/wiki/Algorithms-Database)
  - [Conda](https://github.com/PARC-projects/video-query-home/wiki/Algorithms-Conda)
  - [Broker](https://github.com/PARC-projects/video-query-home/wiki/Algorithms-Broker)

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull
requests to us.

## Credits

Include a citation for a paper when we publish one.  For now:
If you find this repository useful, please cite
[https://github.com/PARC-projects/video-query-home](https://github.com/PARC-projects/video-query-home).

#### Project team
Software development:
- [Frank Torres](https://github.com/fetorres)
- [Chad Ramos](https://github.com/chad-ramos)

Algorithm development by Frank Torres, Matthew Shreve, Gaurang Ganguli and Hoda Eldardiry.

## License

Copyright (C) 2018 Palo Alto Research Center, Inc.

This program is free software for non-commercial uses: you can redistribute it and/or modify
it under the terms of the Aladdin Free Public License - see the [LICENSE.md](LICENSE.md) file for details.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

If this license does not meet your needs, please submit an Issue on github with
your contact information and institution, or email engage@parc.com, so we can discuss how to meet your needs.
