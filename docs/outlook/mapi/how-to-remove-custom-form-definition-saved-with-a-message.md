---
title: Entfernen benutzerdefinierter Formulardefinitionen, die mit einer Nachricht gespeichert wurden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: ac162cb73cfdee83bf034de32064c5ed9df3bc02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408467"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a><span data-ttu-id="bf0e5-103">Entfernen benutzerdefinierter Formulardefinitionen, die mit einer Nachricht gespeichert wurden</span><span class="sxs-lookup"><span data-stu-id="bf0e5-103">Remove custom form definition saved with a message</span></span>
  
<span data-ttu-id="bf0e5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf0e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf0e5-105">In diesem Thema wird ein Codebeispiel in C++ gezeigt, das eine Nachricht, die mit einer benutzerdefinierten Formulardefinition gespeichert wurde, in eine reguläre Nachricht ohne Formulardefinition konvertiert.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-105">This topic shows a code sample in C++ that converts a message that has been saved with a custom form definition to a regular message without the form definition.</span></span>
  
<span data-ttu-id="bf0e5-106">In Microsoft Outlook 2010 oder Microsoft Outlook 2013 können Sie Formulare mit benutzerdefinierten Formularseiten freigeben, indem Sie sie entweder in einer Formularbibliothek veröffentlichen oder die entsprechende Formulardefinition mit einer Nachricht speichern.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-106">In Microsoft Outlook 2010 or Microsoft Outlook 2013, you can share forms containing custom form pages by either publishing them to a forms library or saving the corresponding form definition with a message.</span></span> <span data-ttu-id="bf0e5-107">Ein benutzerdefiniertes Formular, das mit einer Nachricht gespeichert wurde, wird häufig als "einmalformular" bezeichnet, da das Formular nur zum Anzeigen dieser bestimmten Nachricht als einmal verwendete Instanz freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-107">A custom form saved with a message is commonly referred as a "one-off form", since the form is shared only for viewing that specific message as a one-off instance.</span></span> <span data-ttu-id="bf0e5-108">Dies geschieht in der Regel, wenn das Formular nicht in einer Formularbibliothek veröffentlicht wird, der Empfänger jedoch das benutzerdefinierte Formular verwenden soll, wenn das Element geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-108">You typically do this when the form is not published in a forms library but you want the recipient to use the custom form when opening the item.</span></span> <span data-ttu-id="bf0e5-109">Sie können angeben, dass ein Formular im Formular-Designer  eine Einmalvorlage ist,  indem Sie auf der Seite Eigenschaften des Formulars das Kontrollkästchen Formulardefinition mit Element senden aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-109">You can specify a form is a one-off in the Forms Designer, by selecting the **Send form definition with item** check box on the **Properties** page of the form.</span></span> 
  
<span data-ttu-id="bf0e5-110">Formulare, die Formularseiten enthalten, können mit Code in Visual Basic Scripting Edition (VBScript) angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-110">Forms containing form pages can be customized with code in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="bf0e5-111">Nachrichten, die mit Formulardefinitionen gespeichert werden, sind im Allgemeinen größer.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-111">Messages that are saved with form definitions are generally bigger in size.</span></span> <span data-ttu-id="bf0e5-112">Aus Sicherheits- und Speichergründen Outlook 2010 und Outlook 2013 Formulardefinitionen ignorieren, die mit einem beliebigen Element gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-112">For security and storage reasons, Outlook 2010 and Outlook 2013 ignore form definitions saved with any item.</span></span>
  
<span data-ttu-id="bf0e5-113">Um eine Nachricht, die mit einer benutzerdefinierten Formulardefinition gespeichert ist, in eine ohne zu konvertieren, müssen Sie vier benannte Eigenschaften entfernen:</span><span class="sxs-lookup"><span data-stu-id="bf0e5-113">To convert a message that is saved with a custom form definition to one without, you must remove four named properties:</span></span>
  
- [<span data-ttu-id="bf0e5-114">Kanonische PidLidFormStorage-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bf0e5-114">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="bf0e5-115">Kanonische PidLidPageDirStream-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bf0e5-115">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="bf0e5-116">Kanonische PidLidFormPropStream-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bf0e5-116">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="bf0e5-117">Kanonische PidLidScriptStream-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bf0e5-117">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
<span data-ttu-id="bf0e5-118">Darüber hinaus sollten Sie auch die [kanonische PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) entfernen, die die Definitionen von benutzerdefinierten Eigenschaften enthält, die mit dieser Nachricht gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-118">In addition, you should also remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) that contains the definitions of custom properties saved with that message.</span></span> <span data-ttu-id="bf0e5-119">Ein Nebeneffekt des Entfernens dieser Eigenschaft ist, dass die Outlook 2010- oder Outlook 2013-Objektmodelle und die Benutzeroberfläche von Outlook 2010 oder Outlook 2013 nicht mehr auf Benutzereigenschaften zugreifen können, die für die Nachricht festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-119">A side effect of removing this property is that the Outlook 2010 or Outlook 2013 object models and the Outlook 2010 or Outlook 2013 user interface will no longer be able to access user properties that have been set on the message.</span></span> <span data-ttu-id="bf0e5-120">Sie können weiterhin über MAPI auf diese Eigenschaften und deren Werte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-120">You are still able to access these properties and their values through MAPI.</span></span> <span data-ttu-id="bf0e5-121">Wenn Sie diese Eigenschaft nicht entfernen und die Nachricht mit einer anderen Formulardefinition gespeichert wird, wird die [kanonische PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) teilweise mit neuen Daten überschrieben, und die Datenintegrität ist nicht garantiert.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-121">Note that if you do not remove this property and the message is saved with another form definition, the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) is partially overwritten with new data and data integrity is not guaranteed.</span></span> 
  
<span data-ttu-id="bf0e5-122">Wenn Sie die [kanonische PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md)entfernen,  sollten Sie auch das INSP_PROPDEFINITION aus der kanonischen [Eigenschaft PidLidCustomFlag entfernen.](pidlidcustomflag-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="bf0e5-122">If you remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md), then you should also remove the **INSP_PROPDEFINITION** flag from the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md).</span></span>
  
<span data-ttu-id="bf0e5-123">Die folgende Funktion akzeptiert als Eingabeparameter einen Zeiger auf eine Nachricht und einen Indikator, ob die `RemoveOneOff` [kanonische Eigenschaft PidLidPropertyDefinitionStream entfernt werden soll.](pidlidpropertydefinitionstream-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="bf0e5-123">The following function,  `RemoveOneOff`, accepts as input parameters a pointer to a message and an indicator whether to remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md).</span></span> <span data-ttu-id="bf0e5-124">Mithilfe des Nachrichtenzeigers ruft er [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) auf, um die entsprechenden Eigenschaftenbezeichner zu erhalten, und ruft dann [IMAPIProp::D eleteProps](imapiprop-deleteprops.md) auf, um die benannten Eigenschaften zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-124">Using the message pointer, it calls [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the appropriate property identifiers, and then calls [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) to remove the named properties.</span></span> <span data-ttu-id="bf0e5-125">Außerdem ruft sie [IMAPIProp::GetProps](imapiprop-getprops.md) auf, um die [kanonische PidLidCustomFlag-Eigenschaft](pidlidcustomflag-canonical-property.md) zu erhalten, und entfernt das **INSP \_ ONEOFFFLAGS-Flag** und **das INSP_PROPDEFINITION-Flag** aus dieser Eigenschaft, sodass Outlook 2010 und Outlook 2013 nicht nach den benannten Eigenschaften sucht, die entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-125">It also calls [IMAPIProp::GetProps](imapiprop-getprops.md) to get the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md) and clears the **INSP\_ONEOFFFLAGS** flag and **INSP_PROPDEFINITION** flag as appropriate from that property, so that Outlook 2010 and Outlook 2013 will not look for those named properties that have been removed.</span></span> 
  
```cpp
ULONG aulOneOffIDs[] = {dispidFormStorage,  
    dispidPageDirStream, 
    dispidFormPropStream, 
    dispidScriptStream, 
    dispidPropDefStream, // dispidPropDefStream must remain next to last in list 
    dispidCustomFlag};   // dispidCustomFlag must remain last in list 
 
#define ulNumOneOffIDs (sizeof(aulOneOffIDs)/sizeof(aulOneOffIDs[0])) 
 
HRESULT RemoveOneOff(LPMESSAGE lpMessage, BOOL bRemovePropDef) 
{ 
    if (!lpMessage) return MAPI_E_INVALID_PARAMETER; 
     
    HRESULT hRes = S_OK; 
    MAPINAMEID  rgnmid[ulNumOneOffIDs]; 
    LPMAPINAMEID rgpnmid[ulNumOneOffIDs]; 
    LPSPropTagArray lpTags = NULL; 
 
    ULONG i = 0; 
    for (i = 0 ; i < ulNumOneOffIDs ; i++) 
    { 
        rgnmid[i].lpguid = (LPGUID)&PSETID_Common; 
        rgnmid[i].ulKind = MNID_ID; 
        rgnmid[i].Kind.lID = aulOneOffIDs[i]; 
        rgpnmid[i] = &rgnmid[i]; 
    } 
   
    hRes = lpMessage->GetIDsFromNames( 
        ulNumOneOffIDs, 
        rgpnmid, 
        0, 
        &lpTags); 
    if (lpTags) 
    { 
        // The last prop is the flag value  
        // to be updated, don't count it 
        lpTags->cValues = ulNumOneOffIDs-1; 
 
        // If the prop def stream is not to be removed, don't count it 
        if (!bRemovePropDef) 
        { 
          lpTags->cValues = lpTags->cValues-1; 
        } 
 
        hRes = lpMessage->DeleteProps( 
            lpTags, 
            0); 
        if (SUCCEEDED(hRes)) 
        { 
            SPropTagArray pTag = {0}; 
            ULONG cProp = 0; 
            LPSPropValue lpCustomFlag = NULL; 
 
            // Grab dispidCustomFlag, the last tag in the array 
            pTag.cValues = 1; 
            pTag.aulPropTag[0] = CHANGE_PROP_TYPE( 
                lpTags->aulPropTag[ulNumOneOffIDs-1], 
                PT_LONG); 
 
            hRes = lpMessage->GetProps( 
                &pTag, 
                fMapiUnicode, 
                &cProp, 
                &lpCustomFlag); 
            if (SUCCEEDED(hRes) &&  
                1 == cProp && lpCustomFlag &&  
                PT_LONG == PROP_TYPE(lpCustomFlag->ulPropTag)) 
            { 
                // Clear the INSP_ONEOFFFLAGS bits so Outlook  
                // doesn't look for the props that have been deleted 
                lpCustomFlag->Value.l =  
                    lpCustomFlag->Value.l & ~(INSP_ONEOFFFLAGS); 
                if (bRemovePropDef) 
                { 
                    lpCustomFlag->Value.l =  
                        lpCustomFlag->Value.l & ~(INSP_PROPDEFINITION); 
                } 
                hRes = lpMessage->SetProps( 
                    1, 
                    lpCustomFlag, 
                    NULL); 
             } 
 
             hRes = lpMessage->SaveChanges(KEEP_OPEN_READWRITE); 
         } 
    } 
    MAPIFreeBuffer(lpTags); 
 
    return hRes; 
}
```

## <a name="see-also"></a><span data-ttu-id="bf0e5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf0e5-126">See also</span></span>

- [<span data-ttu-id="bf0e5-127">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="bf0e5-127">MAPI Constants</span></span>](mapi-constants.md)

