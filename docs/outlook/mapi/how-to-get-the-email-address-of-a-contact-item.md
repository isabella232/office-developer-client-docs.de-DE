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
# <a name="get-the-email-address-of-a-contact-item"></a><span data-ttu-id="9c9f4-103">Abrufen der E-Mail-Adresse eines Kontaktelements</span><span class="sxs-lookup"><span data-stu-id="9c9f4-103">Get the email address of a Contact item</span></span>

<span data-ttu-id="9c9f4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c9f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c9f4-105">In diesem Thema wird gezeigt, wie Sie den Wert einer benannten Eigenschaft abrufen, die die e-Mail-Adresse eines Microsoft Outlook 2010-oder Microsoft Outlook 2013-Kontaktelements darstellt.</span><span class="sxs-lookup"><span data-stu-id="9c9f4-105">This topic shows how to obtain the value of a named property that represents the email address of an Microsoft Outlook 2010 or Microsoft Outlook 2013 Contact item.</span></span>
  
<span data-ttu-id="9c9f4-106">Sie können bis zu drei e-Mail-Adressen einem Kontaktelement in Outlook 2010 und Outlook 2013 zuordnen.</span><span class="sxs-lookup"><span data-stu-id="9c9f4-106">You can associate up to three email addresses with a Contact item in Outlook 2010 and Outlook 2013.</span></span> <span data-ttu-id="9c9f4-107">Jede e-Mail-Adresse entspricht einer Eigenschaft des **ContactItem** -Objekts von Outlook 2010 oder Outlook 2013 in den Objektmodellen Outlook 2010 und Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="9c9f4-107">Each email address corresponds to a property of the Outlook 2010 or Outlook 2013 **ContactItem** object in the Outlook 2010 and Outlook 2013 object models.</span></span> <span data-ttu-id="9c9f4-108">Intern für Outlook 2010 und Outlook 2013 entspricht die e-Mail-Adresse auch einer benannten MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9c9f4-108">Internal to Outlook 2010 and Outlook 2013, the email address also corresponds to a MAPI named property.</span></span> <span data-ttu-id="9c9f4-109">Beispielsweise entspricht die erste e-Mail-Adresse eines Kontakts der **Email1Address** -Eigenschaft des **ContactItem** im Outlook 2010-und Outlook 2013-Objektmodell und dem internen Outlook 2010-und Outlook 2013-Namen [ Pidlidemail1emailaddress (-kanonische Eigenschaft](pidlidemail1emailaddress-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="9c9f4-109">For example, the first email address of a contact corresponds to the **Email1Address** property of the **ContactItem** in the Outlook 2010 and Outlook 2013 object models, and the Outlook 2010 and Outlook 2013 internal named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).</span></span>
  
<span data-ttu-id="9c9f4-110">Um den Wert einer e-Mail-Adresse eines Kontaktelements abzurufen, können Sie das **propertyAccessor** -Objekt des Outlook 2010-oder Outlook 2013-Objektmodells verwenden oder zunächst [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Property-Tag der benannten Eigenschaft abzurufen, und dann Geben Sie dieses Property-Tag in [IMAPIProp::](imapiprop-getprops.md) GetProps an, um den Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9c9f4-110">To obtain the value of an email address of a contact item, you can use the **PropertyAccessor** object of the Outlook 2010 or Outlook 2013 object model, or first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag of the named property, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="9c9f4-111">Geben Sie beim Aufrufen von **IMAPIProp:: GetIDsFromNames**die entsprechenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, auf die durch den Eingabeparameter _lppPropNames_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9c9f4-111">When calling **IMAPIProp::GetIDsFromNames**, specify the appropriate values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_.</span></span> <span data-ttu-id="9c9f4-112">Das folgende Codebeispiel zeigt, wie Sie die erste e-Mail-Adresse eines angegebenen `lpContact`Kontakts abrufen, indem Sie **GetIDsFromNames** und GetProps verwenden. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9c9f4-112">The following code sample shows how to obtain the first email address of a specified contact,  `lpContact`, using **GetIDsFromNames** and **GetProps**.</span></span> 
  
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


