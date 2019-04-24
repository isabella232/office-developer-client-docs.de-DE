---
title: Abrufen der E-Mail-Adresse eines Kontaktelements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: fab09d0c594bac1374973f523abe6ff0b9c09dd0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344688"
---
# <a name="get-the-email-address-of-a-contact-item"></a>Abrufen der E-Mail-Adresse eines Kontaktelements

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird gezeigt, wie Sie den Wert einer benannten Eigenschaft abrufen, die die e-Mail-Adresse eines Microsoft Outlook 2010-oder Microsoft Outlook 2013-Kontaktelements darstellt.
  
Sie können bis zu drei e-Mail-Adressen einem Kontaktelement in Outlook 2010 und Outlook 2013 zuordnen. Jede e-Mail-Adresse entspricht einer Eigenschaft des **ContactItem** -Objekts von Outlook 2010 oder Outlook 2013 in den Objektmodellen Outlook 2010 und Outlook 2013. Intern für Outlook 2010 und Outlook 2013 entspricht die e-Mail-Adresse auch einer benannten MAPI-Eigenschaft. Beispielsweise entspricht die erste e-Mail-Adresse eines Kontakts der **Email1Address** -Eigenschaft des **ContactItem** im Outlook 2010-und Outlook 2013-Objektmodell und dem internen Outlook 2010-und Outlook 2013-Namen [ Pidlidemail1emailaddress (-kanonische Eigenschaft](pidlidemail1emailaddress-canonical-property.md).
  
Um den Wert einer e-Mail-Adresse eines Kontaktelements abzurufen, können Sie das **propertyAccessor** -Objekt des Outlook 2010-oder Outlook 2013-Objektmodells verwenden oder zunächst [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Property-Tag der benannten Eigenschaft abzurufen, und dann Geben Sie dieses Property-Tag in [IMAPIProp::](imapiprop-getprops.md) GetProps an, um den Wert abzurufen. Geben Sie beim Aufrufen von **IMAPIProp:: GetIDsFromNames**die entsprechenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, auf die durch den Eingabeparameter _lppPropNames_verwiesen wird. Das folgende Codebeispiel zeigt, wie Sie die erste e-Mail-Adresse eines angegebenen `lpContact`Kontakts abrufen, indem Sie **GetIDsFromNames** und GetProps verwenden. **** 
  
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


