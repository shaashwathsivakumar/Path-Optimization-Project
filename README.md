# Path-Optimization-Project
### Abstract
Accessibility for the physically disabled is a prevalent issue at UCLA where stairs
and steep slopes make navigating campus arduous. In this project, we aim to
model integral parts of UCLA campus and simulate the paths a wheelchair
user and a control non-disabled individual would take. Using travel time as
the primary metric, we develop two algorithms, Dijkstra’s and least-resistance,
to find optimal paths from selected nodes. We demonstrate how wheelchair

users are dramatically inconvenienced by the lack of accommodations and inef-
ficient ramps which increase their travel times to as much as 6 times the control.

We seek to expand the model’s scope and improve its accuracy in addition to

proposing engineering solutions to make campus more accessible for the physi-
cally disabled.

### Problem Description
Westwood is notoriously hilly and the University of California Los Angeles was
subsequently designed with many stairs and steep pathways to optimize the
area. This often makes the campus inaccessible to physically disabled students
who attempt to navigate primarily through elevators or moderate inclines. Some
integral halls and centers are entirely out of reach for wheelchair users and many
more require lengthy detours. Physically disabled students comprise 2.1% of the

40,000 students at UCLA. Moreover, the influx of students using wheeled trans-
port, including electric scooters and skateboards, has made campus accessibility

an increasingly salient issue. UCLA is one of the largest public universities, host-
ing countless clubs, sports events, international speakers, performing arts, etc.,

and accommodating these populations is necessary for UCLA to encourage at-
tendance and visitation regardless of physical ability.

This project aims to identify and access areas of inaccessibility on UCLA’s
campus, focusing on the most populated routes. For routes that don’t support
wheelchair users, we propose efficient ramps or similar solutions that would not
unreasonably inconvenience disabled students. To highlight inefficient detours,

we map UCLA’s most populated routes, using travel time as a metric of compar-
ison between a simulated wheelchair individual and a non-disabled individual.

This enables us to depict where UCLA’s campus struggles with wheel accessi-
bility by analyzing large disparities in travel time between the two test subjects.
With this data, we can propose efficient alternatives that wheelchair users could
leverage in lieu of stairs or steep inclines. For the current state of campus, we use
path optimization to calculate the fastest and most efficient routes for disabled
individuals for any given destination. The results of the project will promote
inclusivity and equal opportunity for education regardless of physical ability.



### Simplifications
In order to construct our model, we simplify particular elements and abstract
other variables or hold them constant while still trying to preserve the model’s
accuracy. UCLA campus size is roughly 400 acres, and while it would be bene-
ficial to map the entirety of campus, we simplify our area of assessment to the
most integral part of campus that sees the most traffic. This makes data collec-
tion for our model feasible while preserving its viability since the region is where
physically disabled students are most likely to encounter issues. Once the model
is appropriately calibrated, it can also be expanded to represent the entirety of
campus. The simplified region is a rectangle with Bunche Hall, Pritzker Hall,
Ackerman Turnaround, and Anderson School of Management denoting each of
the corners. We select nodes in the rectangular region which mark major intersections
that connect key paths. In everyday scenarios, people navigate from any arbi-
trary point of campus to another but the simplification of using predetermined
nodes allows us to employ graph theory and streamline data collection. The
nodes will preserve the model’s efficacy because any outdoor point in the rect-
angle can be reach through the nodes.
In the path optimization model, we will simulate a physically disabled and
a non-disabled individual. To simplify the physically disabled simulation, we
use a hypothetical non-motorized wheelchair user as the standard when con-
sidering factors like speed and necessary accommodations. Though there are
a vast array of transport options for the physically disabled, each with their
own characteristics, the wheelchair user would encompass the majority of them
with the intended use of the model. Wheelchair accessibility would also be re-
flective of the preferences of scooters, skateboards, and other wheeled transport.
In order to consistently measure time for our wheelchair and non-disabled in-
dividuals, we make assumptions about their pace and endurance. For wheelchair
users, we assume an average speed of 2 miles per hour and 3 miles per hour for
the non-disabled individual. The average speeds may be reductive as individu-
als have varying speeds, especially for the wheelchairs when paired with motors.
However, the aim of this project is to compare the ratios of times between differ-
ent routes for disabled versus able-bodied, making raw times less relevant. We
assume no fatigue, making pace consistent irrespective of the length and rigor
of the route. Though this may introduce inaccuracies as many students prefer
to avoid stairs and leverage elevators regardless of physical ability, it would be
difficult to factor this into the model and provides little benefit for its intended
purpose. We also assume a natural gradient of pace decrease when walking up
slopes. To represent whether a given destination is accessible via wheelchair,
we employ a binary system where 0 represents inaccessibility. Moreover, we
assume any route which requires an incline above 30 degrees is inaccessible for



the wheelchair user.
