---
title: Abrufen der e-Mail-Adresse eines Kontaktelements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: ce9579cb6b07336cae7d69fe503c918d96946b0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791850"
---
# <a name="get-the-email-address-of-a-contact-item"></a>Abrufen der e-Mail-Adresse eines Kontaktelements

**Betrifft**: Outlook 
  
In diesem Thema veranschaulicht, wie den Wert einer benannten Eigenschaft abrufen, die e-Mail-Adresse eines Microsoft Outlook 2010 oder Microsoft Outlook 2013 Kontakt Elements darstellt.
  
Sie können bis zu drei e-Mail-Adressen mit einem Kontaktelement in Outlook 2010 und Outlook 2013 zuordnen. Jede e-Mail-Adresse entspricht einer Eigenschaft des Outlook 2010 oder Outlook 2013 **ContactItem** -Objekts in Outlook 2010 und Outlook 2013-Objektmodellen. Interne für Outlook 2010 und Outlook 2013, entspricht die e-Mail-Adresse auch eine benannte Eigenschaft MAPI. Beispielsweise entspricht die **Email1Address** -Eigenschaft des **ContactItem** in Outlook 2010 und Outlook 2013 Objektmodelle und die Outlook 2010 und Outlook 2013 interne benannten [die erste e-Mail-Adresse eines Kontakts Kanonische PidLidEmail1EmailAddress-Eigenschaft](pidlidemail1emailaddress-canonical-property.md).
  
Um den Wert der eine e-Mail-Adresse eines Kontaktelements zu erhalten, können Sie verwenden Sie das **PropertyAccessor** -Objekt des Outlook 2010 oder Outlook 2013-Objektmodells oder zuerst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschafts-Tag der benannten Eigenschaft abzurufen und dann Geben Sie diese Eigenschaftentag in [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen des Werts. Beim Aufruf von **IMAPIProp::GetIDsFromNames**, geben Sie die entsprechenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, das Eingabeparameter _LppPropNames_auf zeigt. Das folgende Codebeispiel zeigt, wie die erste e-Mail-Adresse eines angegebenen Kontakts, erhalten `lpContact`, **GetIDsFromNames** und **GetProps**verwenden. 
  
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


