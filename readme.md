#AirLST Widget

__Keywords:__ Restaurant, Reservation, Booking, Widget, Online, Reservation

##Summary
AirLST (pronounced *airlist*) allows you to easily accept online reservations from your website. AirLST Widget can be integrated with one single line of javascript. The user interface is responsive and seamlessly works on mobile phones, tablet and standard desktop screens.

##Usage
Integrating AirLST widget is as easy as copying two snippets of javascript to your page: A loader and the actual link. This advanced method differs a bit from the simple method that is provided in the AirLST Admin Backend.

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
AirLst widget can be customized using additional parameters on the ``<a>``-Tag. Here's the list of optional parameters:

### data-widget-key
Use ```data-widget-key=""``` with your custom widget-key, which can be found in the admin panel.

**Example:**

	data-widget-key="hDjSkSkD"

### data-rsvplist-id (optional)
The default widget for guestlists offers a drop down menu on the first screen, where the user can choose the appropriate guestlist to make a reservation on. Use ```data-rsvplist-id=""``` to only display a specific guestlist in the widget. 

**Example:**

	data-rsvplist-id="83728"

### data-text-addon (optional)
With this parameter, you can provide a hidden text, which will be attached to the reservation. It is best used to send additional information back to the recipient of the request (for example, to your guest relations manager), which should not be visible to the guest.

Example usage would be:
- You have different reservation websites and want to track from which website the reservation is coming
- You offer two separate widgets for smoker and non-smoker reservations

**Example:**

	data-text-addon="Reservierung für Club"


### data-field-phone (optional)
The default widget requires the user to enter a telephone number. You can either make this field optional or hide it completely by specifying ```data-field-phone```.

* ```data-field-phone="require"``` Requires phone number
* ```data-field-phone="display"``` Display the phone number field, but don't require an input
* ```data-field-phone="hide"``` Hide the phone number field completely

### data-field-msg-request (optional)
The default widget allows the user to enter a comment for this reservation. You can hide this comment field by using parameter ```data-field-msg-request```.

* ```data-field-msg-request="display"``` Show the comment field
* ```data-field-msg-request="hide"``` Hide the comment field

### data-field-additional (optional)
You can add one custom field to be entered by the user during registration.

* ```data-field-additional="require"``` Make input for the additional field required
* ```data-field-phone="display"``` Just display the additional field, but don't require input
* ```data-field-phone="hide"``` Hide the additional field

**Please Note:** To use the addtional field, you have to provide a label for it (see next parameter ```data-field-additional-label```).

### data-field-additional-label (optional)
With this parameters, you can specify how the additional field should be called.

**Example:**

	data-additional-field-label="Firma"


### data-button-text (optional)
The default widget uses the text "Jetzt reservieren!" on the submit button on the last screen. Use ```data-button-text``` to change this text.

**Example:**

	data-button-text="Jetzt rückmelden!"
	
### data-date-rsvp-min
With this parameter, you can specify a minimum date for calendar reservations. You can use it to only allow reservations after a certain date, for example if the opening of your venue is in the future.

**Example:**
	
	data-date-rsvp-min="20140620"
	
This will block reservations before June 20th, 2014. 

	Syntax for dates: YYYYMMDD

### data-date-rsvp-max
With this parameter, you can specify a maximum date for calendar reservations. You can use it to only allow reservations before a certain date, for example if your venure closes in a few weeks.

**Example:**
	
	data-date-rsvp-max="20140930"
	
This will block reservations after September 30th, 2014. 

	Syntax for dates: YYYYMMDD
	
### class="airlst-style" (optional)
If you would like to render your reservation link in the classic AirLST-Button style (blue button with white typo), simply add ```airlst-style```to the class-attribute of the element. Be careful not to remove the ```airlst-button```class from the element.

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

[LINKS DER ISAR](http://www.linksderisar.com) ist eine [Digitalagentur](http://www.linksderisar.com) aus München.