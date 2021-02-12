# My First Microfrontends Project

- The project is imaginary tractor toys producing startup
- Two teams are created. Team Decide will create `tractor detail page` and Team Inspire will create `recommendation` page. So we have a product page and a recommendation page for every model
  
## Getting Started

### Freedom of choosing technology
- Team Decide will use node server with server side rendering
- Team inspire will use python and machine learning server
  
### Independent Deployment for both teams



* Download the source code and run it

## page link transitions

### Data Ownership
- Team decide owns products data. they create api for its creation, updates and hosting
- Team inspire regularly poll for this data 

### Contract between the teams ( base on URL )
- Decide => /product/:sku 
- Inspire => /recommendation/:sku
- The integration works because both teams exchanged their URL patterns before-hand

## Composition via Iframes
- Now teams decide that integration via iframe can be a good options
- Team Inspire have to remove the `Tractor` header
- Team decide will embed the iframe along with some CSS for the iframe
- Now Team Inspire is bounded by Team decide for height of Iframe/ products they want to show
  
### Iframe Drawbacks
- Layout Constraint => auto height adjustment problem
- performance overhead ( each iframe creates new browsing context)
- bad accessiblity like ereaders dont know what is going on when iframes are used
- bad for search engines
  

