# Strapi CMS Setup for DryerMaster.com

## **Table of Contents**

1. [Introduction](#introduction)
2. [Project Overview](#project-overview)
3. [Content Types and Fields](#content-types-and-fields)
4. [Dynamic Zones and Components](#dynamic-zones-and-components)
5. [API Integration with Next.js](#api-integration-with-nextjs)
6. [Development Workflow](#development-workflow)
7. [Future Enhancements](#future-enhancements)

---

## **Introduction**

This document outlines the configuration and content structure of Strapi CMS for DryerMaster.com. It provides detailed information about the content types, dynamic zones, and integration strategy with the Next.js framework.

---

## **Project Overview**

- **CMS**: Strapi (headless CMS for content management).
- **Frontend**: Next.js for a dynamic and SEO-friendly website.
- **Purpose**: Efficiently manage static and dynamic assets for DryerMaster.com.
- **Key Features**:
  - Scalable content architecture.
  - Reusable components for consistency.
  - SEO optimization through dynamic meta fields.

---

## **Content Types and Fields**

### **Single Types**

#### 1. Global

- **Header**:
  - Logo (Media)
  - Navigation Links (JSON or Relation)
- **Footer**:
  - Social Links (JSON)
  - Copyright Text (Text)
- **SEO Defaults**:
  - Meta Title (Text)
  - Meta Description (Text)
  - OG Image (Media)

#### 2. Homepage

- **Hero Section**:
  - Title (Text)
  - Subtitle (Text)
  - Background Image (Media)
  - CTA Button (Text, URL)
- **Features**:
  - Title (Text)
  - Description (Text)
  - Icon/Image (Media)
- **Testimonials**:
  - Relation to Testimonial Collection
- **SEO**:
  - Meta Title (Text)
  - Meta Description (Text)
  - OG Image (Media)

#### 3. About Us

- **Title** (Text)
- **Description** (Rich Text)
- **Team Members**:
  - Relation to Team Member Collection
- **Media** (Images/Videos)
- **SEO**:
  - Meta Title (Text)
  - Meta Description (Text)
  - OG Image (Media)

#### 4. Contact Us

- **Address** (Text)
- **Phone Number** (Text)
- **Email** (Email)
- **Google Maps Embed** (Text/JSON)
- **SEO**:
  - Meta Title (Text)
  - Meta Description (Text)
  - OG Image (Media)

### **Collection Types**

#### 1. Blog

- Title (Text)
- Slug (UID)
- Content (Rich Text/Markdown)
- Featured Image (Media)
- Author (Relation to Author Collection)
- Category (Relation to Category Collection)
- Tags (Relation to Tag Collection)
- Publish Date (Date)
- SEO (Meta Title, Meta Description, OG Image)

#### 2. Products

- Name (Text)
- Slug (UID)
- Short Description (Text)
- Full Description (Rich Text)
- Features (Component)
- Technical Specifications (JSON/Rich Text)
- Images (Media Array)
- Related Products (Relation to Product Collection)
- SEO (Meta Title, Meta Description, OG Image)

#### 3. FAQs

- Question (Text)
- Answer (Rich Text)
- Category (Relation to Category Collection)

#### 4. Testimonials

- Quote (Rich Text)
- Author Name (Text)
- Author Role (Text)
- Author Company (Text)
- Author Image (Media)

#### 5. Case Studies

- Title (Text)
- Slug (UID)
- Overview (Rich Text)
- Results (Rich Text)
- Media (Images/Videos)
- SEO (Meta Title, Meta Description, OG Image)

#### 6. Team Members

- Name (Text)
- Role (Text)
- Profile Image (Media)
- Biography (Rich Text)

#### 7. Categories

- Name (Text)
- Slug (UID)
- Description (Rich Text)

#### 8. Tags

- Name (Text)
- Slug (UID)

---

## **Dynamic Zones and Components**

### **Reusable Components**

- **Feature Component**:
  - Title (Text)
  - Description (Text)
  - Icon/Image (Media)
- **SEO Component**:
  - Meta Title (Text)
  - Meta Description (Text)
  - OG Image (Media)
- **Media Gallery**:
  - Images/Videos (Media Array)
  - Description (Text)
- **Slider Component**:
  - Title (Text)
  - Slides (Relation to Media Gallery)

### **Dynamic Zones**

- **Homepage**:
  - Hero Section, Features, Testimonials.
- **Blog Posts**:
  - Rich Text, Media, Quotes.
- **About Us**:
  - Team Members, Rich Text, Media.

---

## **API Integration with Next.js**

- Use Strapi REST or GraphQL API to fetch content.
- **Fetching Strategies**:
  - `getStaticProps` for static pages like Homepage, About Us.
  - `getStaticPaths` for dynamic routes (e.g., Blog, Products).
  - `getServerSideProps` for frequently updated content like FAQs.
  - Incremental Static Regeneration (ISR) for blogs and case studies.
- Optimize image delivery using Next.js Image Optimization.

---

## **Development Workflow**

1. **Strapi Setup**:

   - Install Strapi and configure the CMS.
   - Define content types and fields.
   - Create reusable components and dynamic zones.

2. **Next.js Integration**:

   - Fetch data via API calls.
   - Map Strapi content types to Next.js pages and components.

3. **Content Creation**:

   - Populate static and dynamic content in Strapi.
   - Add SEO metadata for all entries.

4. **Testing**:

   - Ensure all API routes return correct data.
   - Test responsiveness and dynamic routing in Next.js.

5. **Deployment**:
   - Deploy Strapi CMS to a hosting provider (e.g., AWS, Heroku).
   - Deploy Next.js app to a platform like Vercel.

---

## **Future Enhancements**

- Add localization support for multilingual content.
- Integrate advanced analytics and A/B testing tools.
- Enable content versioning and scheduling in Strapi.

---

This document serves as a blueprint for configuring and managing Strapi CMS for DryerMaster.com. Keep it updated as the project evolves.
