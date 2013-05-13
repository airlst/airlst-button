#AirLST Widget

__Keywords:__ Restaurant, Reservation, Booking, Widget, Online, Reservation

##Summary
AirLST (pronounced *airlist*) allows you to easily accept online reservations from your website. AirLST Widget can be integrated with one single line of javascript. The user interface is responsive and seamlessly works on mobile phones, tablet and standard desktop screens.

##Usage
Integrating AirLST widget is as easy as copying two snippets of javascript to your page: A loader and the actual link.

###Loader

Copy & Paste the following code snippet on your page, preferably in the ``<head>`` section.

	<script type="text/javascript">
		(function() {
			var al = document.createElement('script'); al.type = 'text/javascript'; al.async = true;
			al.src = ('https:' == document.location.protocol ? 'https://' : 'http://') + 'www.airlst.com/widget/v2/airlst-button.js';
			var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(al, s);
		})();
	</script>

This will load the AirLST Widget javascript bridge, which will handle the complete reservation process.

###Link

To render a reservation button, use the following code:

	<a href="#" class="airlst-button" data-widget-key="XXX">Make reservation</a>
	
where you have to replace ```XXX``` with your actual widget-key (get it from the AirLST admin panel).

##Parameters
AirLst Widget can be customized using additional parameters on the ``<a>``-Tag. Here's the list of optional parameters:

* __data-widget-key=""__ (mandatory) Use your custom widget-key, which can be found in the admin panel.
* __data-rsvplist-id=""__ Only displays a specific guestlist. Get the id from the admin panel.
* __data-text-addon=""__ This text will be invisibly added to the reservation message. It is best used to send additional information to the recipient of the request, which should not be visible to the user.

##Example implementations
* [Implementation with link/loader](example-with-loader.html)
* [Implementation with classic script-tag](example-with-script-tag.html)

##Real world examples

* [Bar Reichenbach, München](http://www.bar-reichenbach.de)
* [Cocco Bello, Ludwigsburg](http://www.cocco-bello.de)
* [Spezlwirtschaft, München](http://www.spezlwirtschaft.me)
* [Gasthaus Ruhmöller, Saerbeck](http://www.ruhmoeller.com)

##Prerequisites

To use AirLST, sign up for a free test account. You can manage reservations through our app and web backend (paid). Accepting reservations by email is free of charge and will always be.

Details on [www.AirLST.com](http://www.airlst.com/web/reservationbook)

(English version will be available shortly)

##Copyright
2011-2013 AirLST by LINKS DER ISAR GmbH

All rights reserved. AirLST is a registered trademark of LINKS DER ISAR GmbH.