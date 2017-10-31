# User Inquiries Results ViriCiti Native App
## Breytner
Breytner is a company with four electric transport trucks. They don't look as much on a daily basis to a lot of data or reports. They're main concern is that the trucks charge overnight. If a truck doesn't charge (correctly) overnight they have a serious problem.

I discussed what we could add in the app to provide them with the information they needed in the easiest way possible. At the moment, you can see if a vehicle is charging. I assumed that that was enough. It turns out that that isn't enough. They usually look up the graph of the battery charging. This way they can see if there is a sudden drop in charging rate. This sometimes happens due to faulty charging cables. When this happens and they don't notice it they can get into trouble. They're trucks need to be charged because of the small size of their fleet. Two not fully charged trucks can cause serious problems. Because of this I want to implement the graph in the app. Currently the gauges with speed and state of charge are shown on the vehicle page. This doesn't make sense when the vehicle is charging. The speed will always be 0 and the soc will go up slowly. I want to take a look at showing the graph instead when the vehicle is charging. It's a small change, with a lot of impact.

This discussion led to the other part of the app. They can setup notifications if their trucks aren't charging withing a range of time. They explained that the trucks get connected to the charger at around 8 p.m. and need to be charged the next morning. By creating a notification for this and receiving it on the native app we can help them prevent this issue. It would be very useful if they get a notification that charging is not going as it should. When they click on the notification they should immediately see how the truck has been charging.

It turned out that Breytner needed this feature, but never knew ViriCiti already does this with emails and sms. It is a feature the user wants but doesn't find easily in the portal. Because of this I want to let users setup a notification in the app. This will be a more in your face approach to getting users to make use of this feature.

I will take all the feedback and topics discussed in to account when creating an iteration on the design for the app. The app will be more useful for the user with these modifications.

## Qbuzz
Once Qbuzz gets back to me I will write my findings up.
