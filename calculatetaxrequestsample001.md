# CalculateTaxRequestSample001

```
{
   CalculateTax:{
      Security:{
         Password:'My API Key'
      },      
      Lines:[
         {
            ActualExtendedPrice:100,
            ItemKey:'Shirt001',
            ItemDescription:'A shirt',
            ItemTaxabilityCode:'GENERALMERCHANDISE'
         },
{
            ActualExtendedPrice:10,
            ItemTaxabilityCode:'shipping'
         }
      ],
      DocumentKey:'Order001',
      IsCommited: true,      
       OriginAddress:{
      	Street1:'2854 Nebrina, boulder co 80301',
      	City: 'Boulder',
      	Region: 'CO',
      	PostalCode: '80301'
      },
      DestinationAddress:{
      	Street1:'1877 Broadway, Boulder, CO, 80301',
      	City: 'Boulder',
      	Region: 'CO',
      	PostalCode: '80301'
      }     
   }
}

```