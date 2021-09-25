---
title: Abrufen der E-Mail-Adresse eines Kontaktelements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: ec0adc11a7530cf69f9e7a3bb26f2b8662e21df5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564337"
---
# <a name="get-the-email-address-of-a-contact-item"></a>Abrufen der E-Mail-Adresse eines Kontaktelements

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird erklärt, wie Sie den Wert einer benannten Eigenschaft abrufen, die die E-Mail-Adresse eines Microsoft Outlook 2010- oder Microsoft Outlook 2013 Kontaktelements darstellt.
  
Sie können einem Kontaktelement in Outlook 2010 und Outlook 2013 bis zu drei E-Mail-Adressen zuordnen. Jede E-Mail-Adresse entspricht einer Eigenschaft des Outlook 2010- oder Outlook 2013 **ContactItem-Objekts** in den Objektmodellen Outlook 2010 und Outlook 2013. Intern zu Outlook 2010 und Outlook 2013 entspricht die E-Mail-Adresse auch einer MAPI-Eigenschaft mit dem Namen. Die erste E-Mail-Adresse eines Kontakts entspricht beispielsweise der **Email1Address-Eigenschaft** des **ContactItem-Objekts** in den Objektmodellen Outlook 2010 und Outlook 2013 sowie der internen Outlook 2010- und Outlook 2013-internen [PidLidEmail1EmailAddress-Eigenschaft](pidlidemail1emailaddress-canonical-property.md).
  
Um den Wert einer E-Mail-Adresse eines Kontaktelements abzurufen, können Sie das **PropertyAccessor-Objekt** des Outlook 2010- oder Outlook 2013-Objektmodells verwenden oder zuerst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschaftstag der benannten Eigenschaft abzurufen, und dann dieses Eigenschaftstag in [IMAPIProp::GetProps](imapiprop-getprops.md) angeben, um den Wert abzurufen. Geben Sie beim Aufrufen von **IMAPIProp::GetIDsFromNames** die entsprechenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die durch den Eingabeparameter  _lppPropNames_ verwiesen wird. Das folgende Codebeispiel zeigt, wie die erste E-Mail-Adresse eines angegebenen  `lpContact` Kontakts mithilfe von **GetIDsFromNames** und **GetProps** abgerufen wird. 
  
```cpp
HRESULT HrGetEmail1(LPMESSAGE lpContact) 
{ 
    HRESULT hRes = S_OK; 
    LPSPropTagArray lpNamedPropTags = NULL; 
    MAPINAMEID NamedID = {0}; 
    LPMAPINAMEID lpNamedID = &NamedID; 
    NamedID.lpguid = (LPGUID)&PSETID_Address; 
    NamedID.ulKind = MNID_ID; 
    NamedID.Kind.lID = dispidEmailEmailAddress; 
 
    hRes = lpContact->GetIDsFromNames( 
           1,  
           &lpNamedID,  
           NULL,  
           &lpNamedPropTags); 
 
    if (SUCCEEDED(hRes) && lpNamedPropTags) 
    { 
        SPropTagArray sPropTagArray; 
 
        sPropTagArray.cValues = 1; 
        sPropTagArray.aulPropTag[0] = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[0],PT_STRING8); 
        LPSPropValue lpProps = NULL; 
        ULONG cProps = 0; 
 
        hRes = lpContact->GetProps( 
               &sPropTagArray, 
               NULL, 
               &cProps, 
               &lpProps); 
        if (SUCCEEDED(hRes) &&  
            1 == cProps &&  
            lpProps &&  
            PT_STRING8 == PROP_TYPE(lpProps[0].ulPropTag) && 
            lpProps[0].Value.lpszA) 
        { 
            printf("Email address 1 = \"%s\"\n",lpProps[0].Value.lpszA); 
        } 
        MAPIFreeBuffer(lpProps); 
        MAPIFreeBuffer(lpNamedPropTags); 
     } 
     return hRes; 
}
```


