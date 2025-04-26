# <span font-weight:bold;">Setup IAP on Google Play & App Store</span>

<div class="video-container">
    <iframe width="700" height="405" src="https://www.youtube.com/embed/5L-GKNA6L4M" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

## Introduction

In this video, you'll learn how to set up In-App Purchases (IAP) for your mobile game on Google Play Console and App Store Connect. This step-by-step tutorial walks you through the process of creating in-app products and configuring them correctly on both platforms.

What's Covered

- Setting up in-app products on Google Play Console and App Store Connect

- Key settings and configurations required for successful IAP setup

- Connecting your in-app products with your Unity project

### Setting Up In-App Products on Google Play Console

To offer in-app purchases (IAP) on Google Play, you must configure your products in the Google Play Console.

- Consumable Products: Items like in-game currency or consumables that are used once and can be purchased multiple times. These need to be set up on google play.

- Non-Consumable Products: Items that users buy once and own permanently, such as skins, weapons, or other unlockable content. You will need to configure these for one-time purchases.

- Subscriptions: If you're offering subscriptions, such as recurring premium content or services, you’ll need to configure subscription products with renewal periods (e.g., weekly, monthly, yearly).

Google Play Console allows you to set the pricing, manage localized prices.

###  Setting Up In-App Products on App Store Connect

For iOS applications, Apple uses App Store Connect for managing IAP products.

- Consumables: Just like Google Play, consumable items on iOS are items that can be bought and used (like power-ups, in-game currency, etc.).

- Non-Consumables: These items are permanently available to the user after purchase, such as extra levels, skins, or game features.

- Subscriptions: If you’re offering recurring services, such as a premium membership, these subscriptions are set up with renewal cycles and can provide users with ongoing access to content.

###  Managing IAP Products

Both stores allow you to edit or update your IAP products after they are live. For example, you can:

- Add new in-app products or subscriptions.

- Modify prices or availability.

- Remove or discontinue old products.

This management is essential for keeping your game’s monetization up to date and aligned with any seasonal changes or content updates.

###  Testing Your IAP Products

Before going live with your in-app purchases, you need to test them thoroughly:

Google Play Console: You can create test accounts and simulate purchases, allowing you to verify that everything is working as expected before making it available to the public.

App Store Connect: Apple offers sandbox accounts for testing your in-app purchases. You can make purchases without actually being charged and test the full purchasing flow to ensure that everything is functioning properly.