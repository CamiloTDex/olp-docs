# /shipments/create 👤

Creates an FTL shipment

```ejs
throw "Company not found"
throw "Payment rules not found"
throw "Payment processor not found"

/users/create {
    shipment: {
        origin: {
            address?: string,
            position?: {
                type: "Point",
                coordinates: [lng, lat]
            },
            
            contact?: {
                name: string,
                phone: string,
                ext: string,
                email: string
            },
            
            typeofLocation?: string,
            comments?: string,
            reference?: string,
            additionalInstructions?: string,
         },
            
         stops?: [{
            appointment: { from?: Date, until?: Date },
            location: {
                address?: String;
                position?: Geoposition;
                contact?: ContactInfo;
                typeOfLocation?: string;
                comments?: string;
                reference?: string;
                additionalInstructions?: string;
            }
          }],
          
          destination: {
            address?: string,
            position?: {
                type: "Point",
                coordinates: [lng, lat]
            },
            
            contact?: {
                name: string,
                phone: string,
                ext: string,
                email: string
            },
            
            typeofLocation?: string,
            comments?: string,
            reference?: string,
            additionalInstructions?: string,
         },
         
         payment: {
             rate: number,
             negotiable: boolean,
             rules: "FTLScheduledPayment",
             processor: "none"
         },
         
         appointment: {
             pickup: { from: Date, until: Date },
             arrive: { from: Date, until: Date }
         },
         
         documents: "ftl-usa" | "none",
         commodity?: string,
         weight: number,
         partial?: boolean,
    
         equipments: string[],
         accessorials: { pickup: string[]; arrive: string[]; },

         linearFeet?: number,
         items: [{
            packageType: string;
            pieces: number;
            commodity: string;
            dimensions: {
                width?: number;
                height?: number;
                length?: number;
            }
        
            CBF: number;
            PCF: number;
        
            weight: number;
            shippingClass: string;
            stackable: boolean;
            linearFeet: number;
            hazmat: boolean;
            hazmatDetails: {
                UNNumber: string;
                class: string;
                packingGroup: string;
                properShippingName: string;
                qtyAndtypeOfPackaging: string;
                emergencyNumber: string;
            }
        }]
    },
    token: string
} => {
    username: string,
    role: string,
    companyDID: string,
    did: string
}
```
