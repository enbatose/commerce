<h1>Product Recommendations at Yalo</h1>

![Yalo Logo](/media/yalo_logo.png)

# 🏢 The Company: Yalo - Conversational Commerce

Yalo is an intelligent sales platform powered by Intelligent Agents.

Yalo helps companies sell more and build stronger customer relationships by automating personalized sales across WhatsApp, apps, voice, and more.

# 👨‍💻 The Role: Senior Technical Product Manager

On February 2022 I joined Yalo as a Sr. Technical Product Manager for their Core Services, after successfully completing a number of infrastructure related initiatives I transitioned to be the platform's commerce Product Manager.

As a Commerce Product Manager I managed the Store Front that drove sales through messaging applications, i.e. Whatsapp. The images below depicts a mobile web-based store front.

<center>
  <table border="0" width="600">
    <tr>
      <td width="30%" align="center">
        <img src="/media/mobile_storefront.png" alt="Storefront 1" width="280">
      </td>
      <td width="30%" align="center">
        <img src="/media/mobile_storefront_2.png" alt="Storefront 2" width="280">
      </td>
    </tr>
  </table>
</center>

# 🤖 AI Project: Building the Machine Learning recommendation system

The following sections describe the steps followed in the framework of the CRISP-DM project management schema for AI initiatives.

## Understanding the Business 💵

The **definition of the problem**; the target users are corner shop owners that utilize Yalo's conversational commerce over whatsapp and Yalo's web storefront to purchase inventory to resupply their stores with a vendor's specific product, e.g. Chocolates from Nestlé or Mondelez.

The opportunity being exploited was manifold, (1) Present different product to Store Owners that they have not previously bought but are popular for other store owners in the area (Cross-selling), (2) Remind Store Owners of products they regularly buy but might have forgotten to add to the cart in any given occasion, (3) Suggest better value deals for specific product packages, e.g. a 12 piece pack over a 2 piece pack of a product (Up-selling), (4) Introduce net new products from the vendor (Cold-Start).

The main value proposition resides in the strategy for increasing the average ticket value while helping Store Owners receive a better product mix that will be profitable for them. The current way the Store Owners address the same points are by being requested directly by final customers on specific products they intend to buy, nonetheless, few customers are vocal about a product they didn't find. Further, for net new products or better value pack options, a direct sales person interacts few minutes each week with the Sales Owner, risking missing all the updates. Hence, consolidating the highlights with intelligent product recommendations it's a great opportunity.

The success of the initiative as measured in Average Ticket Value for each purchase, e.g. Increased from ABC to XYZ. Similarly, for net new products, tracking the adoption in sales over time.

## Data Understanding 🧮

The datasets considered were curated for the following purposes:

1. Store Owner historical Purchases
2. Assortment of Products by Store Owner eligibility (E.g. What subset of products are eligible for Store Owner A, that might be different from Store Owner B).
3. Product Attributes, e.g. Category, Packaging Hierarchy (Next/Previous in Size), Short Description, Long Description, Recommended Sell Price, Purchase Cost, New Product Flag, etc.

The following subsections explore in depth the data pipeline experience.

### Gather Data

As described on the Business Understanding section, different models were sought as part of this initiative, each requiring a different dataset to build a model or heuristics logic. The three datasets described above contained all the information needed to model the product recommendations. 

The Data Pipeline created for the data sets mentioned required building middleware integrations with an ERP system to obtain information on the Product Data and consolidate it on Yalo's system. Optionally, the model could use orders placed previously using other CRM systems, or leverage only orders existing on Yalo's system, as the Cold Start problem had been addressed, this didn't represent an issue, unless the B2B customer stated a fixed preference.

### Validate Data

The data cleansing process included validations for integrity and null values. The major gaps in the data were on the Assortment of Products by Store Owner eligibility. Namely, the continuous addition of new Store Owners, being Corner-Stores the main B2B customers, as well as logistics challenges required to dynamically disable certain products to certain stores based on city areas as geo-fenced by Postal Code ranges.

### Explore the Data


• Statistical analysis and
visualization
• Dimensionality
reduction
• Identify relationships
& patterns









