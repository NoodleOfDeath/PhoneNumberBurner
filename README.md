# PhoneNumberBurner
This project demonstrates how simple it is to burn a phone number and also describes how to mitigate such attacks. I am not responsible for any criminal use of this code. It is solely meant for educational purposes. This script when run will send text messages to the specified targets every 2 seconds. Normally several thousand text message requests could be sent per second, but because this utilizes wireless provider API's doing so would cause your server to be blacklisted.

# Usage

	<?php
		
		require_once "PhoneNumberBurner.php";
		
		$targets  = ["8005551234", "8005556789", ];
		$messages = ["Hello World A", "Hello World B", "Hello World C", ];
		
		$dos = new PhoneNumberBurner($targets, $messages);
		$dos -> attack(5000);
		
	?>
	
# Mitigation
 
 Apple iPhones at least allow you to filter out phone numbers not in contacts. Sadly,
 not enough people know of this simple fix.
