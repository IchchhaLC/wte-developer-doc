Overriding Template Files
=====

.. _installation:

Cart Page Template

/wp-travel-engine/content-cart.php

.. code-block:: console

   (.venv) $ pip install lumache

Thank you Page Template

/wp-travel-engine/thank-you/thank-you.php
/wp-travel-engine/thank-you/thankyou-remaining-payment.php

Checkout Page Template

/wp-travel-engine/template-checkout-new.php

Template Division:

Header-steps
------------

/wp-travel-engine/checkout/header-steps.php

Mini Cart
------------

/wp-travel-engine/checkout/mini-cart.php

Search Page Template
------------

/wp-travel-engine/template-trip-search-results.php

Search Form:
/wp-travel-engine/template-trip-search-form.php

My Account Page Template
------------

Login Template
------------

/wp-travel-engine/account/form-login.php

Lost Password Template
------------

/wp-travel-engine/account/form-lostpassword.php

Lost Password Confirmation Template
------------

/wp-travel-engine/account/lostpassword-confirm.php

Reset Password Template
------------

/wp-travel-engine/account/form-reset-password.php

Dashboard Page Outer Wrap
------------

/wp-travel-engine/account/content-dashboard.php

Dashboard Tab
------------

/wp-travel-engine/account/tab-content/dashboard.php

Bookings Tab
------------

/wp-travel-engine/account/tab-content/bookings.php

Account Tab
------------

/wp-travel-engine/account/form-edit-account.php

Billing Tab
------------

/wp-travel-engine/account/form-edit-billing.php

Remaining payment from Dashboard
------------

/wp-travel-engine/account/remaining-payment.php

Email Template
------------

Customer Lost Password Email Template
------------

/wp-travel-engine/emails/customer-lost-password.php

Customer New Account Email Template
------------

/wp-travel-engine/emails/customer-new-account.php

Email Header Template
------------

/wp-travel-engine/emails/email-header.php

Email Footer Template
------------

/wp-travel-engine/emails/email-footer.php

Enquiry Template
------------

/wp-travel-engine/emails/enquiry.php

Traveller Information Template
------------

/wp-travel-engine/traveller-information/template-traveler-info.php

Featured Trip Widget Template
------------

/wp-travel-engine/widgets/content-widget-feat-trip.php

Archive Template Files
------------

Taxonomy Pages Template Files
------------

Main Taxonomy Page
------------

/wp-travel-engine/content–template-taxonomy.php

Activities Page
------------

/wp-travel-engine/template-activities.php

Trip Activities Taxonomy Terms
------------

/wp-travel-engine/taxonomy-activities.php

Destination Page
------------

/wp-travel-engine/template-destination.php

Trip Destination Taxonomy Terms
------------

/wp-travel-engine/taxonomy-destination.php

Trip Types Page
------------

/wp-travel-engine/template-trip_types.php

Trip Types Taxonomy Terms
------------

/wp-travel-engine/taxonomy-trip_types.php

Trip Archive Page
------------

/wp-travel-engine/archive-trip.php

Posts Layout

Grid Layout
------------

/wp-travel-engine/content-grid.php

List Layout
------------

/wp-travel-engine/content-list.php

Sidebar
------------

/wp-travel-engine/template-trip-filters-sidebar.php

Single Trip Page Template
------------

Single Trip Page
------------

/wp-travel-engine/single-trip.php

Single Trip Page Content Wrapper Start
------------

/wp-travel-engine/trip-content-wrapper-start.php

Trip Content
------------

/wp-travel-engine/content-single-trip.php

Single Trip Page Title Section
------------

/wp-travel-engine/single-trip/title.php

Single Trip Page Gallery Section
------------

/wp-travel-engine/single-trip/gallery.php

Single Trip Video Popup Layout
------------

/wp-travel-engine/single-trip/gallery-video-popup.php

Single Trip Video Slider
------------

/wp-travel-engine/single-trip/gallery-video-slider.php

Single Trip Page Inner Content Wrapper
------------

/wp-travel-engine/single-trip/trip-content.php

Single Trip Page Tabs Navigation Section
------------

/wp-travel-engine/single-trip/tabs-nav.php

Single Trip Page Tabs Content Section
------------

/wp-travel-engine/single-trip/tabs-content.php

Single Trip Footer
------------

/wp-travel-engine/single-trip/trip-footer.php

After trip content
------------

/wp-travel-engine/trip-content-wrapper-end.php

Single Trip Sidebar
------------

/wp-travel-engine/single-trip/trip-sidebar.php

Single Trip Tabs
------------

Overview Tab
------------

/wp-travel-engine/single-trip/trip-tabs/overview.php

Itinerary Tab
------------

/wp-travel-engine/single-trip/trip-tabs/itinerary-tab.php

Cost Tab
------------

/wp-travel-engine/single-trip/trip-tabs/cost.php

FAQs Tab
------------

/wp-travel-engine/single-trip/trip-tab/faqs.php

Map Tab
------------

/wp-travel-engine/single-trip/trip-tabs/map.php

Review Tab
------------

/wp-travel-engine/single-trip/trip-tabs/review.php

.. To retrieve a list of random ingredients,
.. you can use the ``lumache.get_random_ingredients()`` function:

.. .. autofunction:: lumache.get_random_ingredients

.. The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
.. or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
.. will raise an exception.

.. .. autoexception:: lumache.InvalidKindError

.. For example:

.. >>> import lumache
.. >>> lumache.get_random_ingredients()
.. ['shells', 'gorgonzola', 'parsley']

