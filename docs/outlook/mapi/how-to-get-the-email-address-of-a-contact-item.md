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
# <a name="get-the-email-address-of-a-contact-item"></a><span data-ttu-id="6c603-103">Abrufen der e-Mail-Adresse eines Kontaktelements</span><span class="sxs-lookup"><span data-stu-id="6c603-103">Get the email address of a Contact item</span></span>

<span data-ttu-id="6c603-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6c603-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6c603-105">In diesem Thema veranschaulicht, wie den Wert einer benannten Eigenschaft abrufen, die e-Mail-Adresse eines Microsoft Outlook 2010 oder Microsoft Outlook 2013 Kontakt Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="6c603-105">This topic shows how to obtain the value of a named property that represents the email address of an Microsoft Outlook 2010 or Microsoft Outlook 2013 Contact item.</span></span>
  
<span data-ttu-id="6c603-106">Sie können bis zu drei e-Mail-Adressen mit einem Kontaktelement in Outlook 2010 und Outlook 2013 zuordnen.</span><span class="sxs-lookup"><span data-stu-id="6c603-106">You can associate up to three email addresses with a Contact item in Outlook 2010 and Outlook 2013.</span></span> <span data-ttu-id="6c603-107">Jede e-Mail-Adresse entspricht einer Eigenschaft des Outlook 2010 oder Outlook 2013 **ContactItem** -Objekts in Outlook 2010 und Outlook 2013-Objektmodellen.</span><span class="sxs-lookup"><span data-stu-id="6c603-107">Each email address corresponds to a property of the Outlook 2010 or Outlook 2013 **ContactItem** object in the Outlook 2010 and Outlook 2013 object models.</span></span> <span data-ttu-id="6c603-108">Interne für Outlook 2010 und Outlook 2013, entspricht die e-Mail-Adresse auch eine benannte Eigenschaft MAPI.</span><span class="sxs-lookup"><span data-stu-id="6c603-108">Internal to Outlook 2010 and Outlook 2013, the email address also corresponds to a MAPI named property.</span></span> <span data-ttu-id="6c603-109">Beispielsweise entspricht die **Email1Address** -Eigenschaft des **ContactItem** in Outlook 2010 und Outlook 2013 Objektmodelle und die Outlook 2010 und Outlook 2013 interne benannten [die erste e-Mail-Adresse eines Kontakts Kanonische PidLidEmail1EmailAddress-Eigenschaft](pidlidemail1emailaddress-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="6c603-109">For example, the first email address of a contact corresponds to the **Email1Address** property of the **ContactItem** in the Outlook 2010 and Outlook 2013 object models, and the Outlook 2010 and Outlook 2013 internal named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).</span></span>
  
<span data-ttu-id="6c603-110">Um den Wert der eine e-Mail-Adresse eines Kontaktelements zu erhalten, können Sie verwenden Sie das **PropertyAccessor** -Objekt des Outlook 2010 oder Outlook 2013-Objektmodells oder zuerst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschafts-Tag der benannten Eigenschaft abzurufen und dann Geben Sie diese Eigenschaftentag in [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen des Werts.</span><span class="sxs-lookup"><span data-stu-id="6c603-110">To obtain the value of an email address of a contact item, you can use the **PropertyAccessor** object of the Outlook 2010 or Outlook 2013 object model, or first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag of the named property, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="6c603-111">Beim Aufruf von **IMAPIProp::GetIDsFromNames**, geben Sie die entsprechenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, das Eingabeparameter _LppPropNames_auf zeigt.</span><span class="sxs-lookup"><span data-stu-id="6c603-111">When calling **IMAPIProp::GetIDsFromNames**, specify the appropriate values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_.</span></span> <span data-ttu-id="6c603-112">Das folgende Codebeispiel zeigt, wie die erste e-Mail-Adresse eines angegebenen Kontakts, erhalten `lpContact`, **GetIDsFromNames** und **GetProps**verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c603-112">The following code sample shows how to obtain the first email address of a specified contact,  `lpContact`, using **GetIDsFromNames** and **GetProps**.</span></span> 
  
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


