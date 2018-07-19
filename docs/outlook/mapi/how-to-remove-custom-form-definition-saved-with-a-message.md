---
title: Entfernen Sie benutzerdefinierter Formulardefinition gespeichert mit einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 9581656c40af39338f8919903f6d0de29c20a061
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791877"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a><span data-ttu-id="80008-103">Entfernen Sie benutzerdefinierter Formulardefinition gespeichert mit einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="80008-103">Remove custom form definition saved with a message</span></span>
  
<span data-ttu-id="80008-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="80008-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="80008-105">In diesem Thema wird ein Codebeispiel in C++, die eine Nachricht konvertiert, die mit der Definition für ein benutzerdefiniertes Formular auf eine reguläre Nachricht ohne die Formulardefinition gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="80008-105">This topic shows a code sample in C++ that converts a message that has been saved with a custom form definition to a regular message without the form definition.</span></span>
  
<span data-ttu-id="80008-106">In Microsoft Outlook 2010 oder Microsoft Outlook 2013 können Sie Formulare mit benutzerdefinierten Formularseiten in einer Formularbibliothek veröffentlichen, oder speichern die entsprechenden Formulardefinition mit einer Nachricht freigeben.</span><span class="sxs-lookup"><span data-stu-id="80008-106">In Microsoft Outlook 2010 or Microsoft Outlook 2013, you can share forms containing custom form pages by either publishing them to a forms library or saving the corresponding form definition with a message.</span></span> <span data-ttu-id="80008-107">Ein benutzerdefiniertes Formular mit einer Nachricht gespeichert wird häufig als "einmaliges Formular," bezeichnet, da das Formular gemeinsam genutzt wird nur für die betreffende Nachricht als einmaligen Instanz anzeigen.</span><span class="sxs-lookup"><span data-stu-id="80008-107">A custom form saved with a message is commonly referred as a "one-off form", since the form is shared only for viewing that specific message as a one-off instance.</span></span> <span data-ttu-id="80008-108">Sie dies in der Regel das Formular wird nicht in einer Formularbibliothek veröffentlicht, aber den Empfänger das benutzerdefinierte Formular beim Öffnen des Elements verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="80008-108">You typically do this when the form is not published in a forms library but you want the recipient to use the custom form when opening the item.</span></span> <span data-ttu-id="80008-109">Sie können angeben, dass ein Formular einer einmaligen im Formular-Designer ist, indem Sie das Kontrollkästchen **Element mit Beschreibung senden** auf der Seite **Eigenschaften** des Formulars auswählen.</span><span class="sxs-lookup"><span data-stu-id="80008-109">You can specify a form is a one-off in the Forms Designer, by selecting the **Send form definition with item** check box on the **Properties** page of the form.</span></span> 
  
<span data-ttu-id="80008-110">Formularen mit Formularseiten können mit Code in Visual Basic Scripting Edition (VBScript) angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="80008-110">Forms containing form pages can be customized with code in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="80008-111">Nachrichten, die mit Formulardefinitionen gespeichert sind sind im Allgemeinen größer Größe.</span><span class="sxs-lookup"><span data-stu-id="80008-111">Messages that are saved with form definitions are generally bigger in size.</span></span> <span data-ttu-id="80008-112">Ignorieren für Sicherheit und Storage Gründe Outlook 2010 und Outlook 2013 Formulardefinitionen mit beliebigen Elements gespeichert.</span><span class="sxs-lookup"><span data-stu-id="80008-112">For security and storage reasons, Outlook 2010 and Outlook 2013 ignore form definitions saved with any item.</span></span>
  
<span data-ttu-id="80008-113">Um eine Nachricht zu konvertieren, die mit der Definition für ein benutzerdefiniertes Formular auf eine ohne gespeichert wird, müssen Sie vier benannte Eigenschaften entfernen:</span><span class="sxs-lookup"><span data-stu-id="80008-113">To convert a message that is saved with a custom form definition to one without, you must remove four named properties:</span></span>
  
- [<span data-ttu-id="80008-114">Kanonische PidLidFormStorage-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="80008-114">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="80008-115">Kanonische PidLidPageDirStream-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="80008-115">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="80008-116">Kanonische PidLidFormPropStream-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="80008-116">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="80008-117">Kanonische PidLidScriptStream-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="80008-117">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
<span data-ttu-id="80008-118">Darüber hinaus sollten Sie auch die [PidLidPropertyDefinitionStream kanonische-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) entfernen, die enthält die Definitionen der benutzerdefinierten Eigenschaften, die mit dieser Nachricht gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="80008-118">In addition, you should also remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) that contains the definitions of custom properties saved with that message.</span></span> <span data-ttu-id="80008-119">Eine Auswirkung dieser Eigenschaft entfernen, die die Objektmodelle von Outlook 2010 oder Outlook 2013 ist und die Benutzeroberfläche von Outlook 2010 oder Outlook 2013 werden nicht mehr Benutzer Eigenschaften zugreifen, die für die Nachricht festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="80008-119">A side effect of removing this property is that the Outlook 2010 or Outlook 2013 object models and the Outlook 2010 or Outlook 2013 user interface will no longer be able to access user properties that have been set on the message.</span></span> <span data-ttu-id="80008-120">Sie können weiterhin auf diese Eigenschaften und deren Werte durch MAPI zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="80008-120">You are still able to access these properties and their values through MAPI.</span></span> <span data-ttu-id="80008-121">Beachten Sie, dass wenn diese Eigenschaft nicht entfernt und die Nachricht mit einem anderen Formulardefinition gespeichert ist, wird die [Kanonische PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) teilweise mit neuen Daten überschrieben und Datenintegrität nicht unbedingt.</span><span class="sxs-lookup"><span data-stu-id="80008-121">Note that if you do not remove this property and the message is saved with another form definition, the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) is partially overwritten with new data and data integrity is not guaranteed.</span></span> 
  
<span data-ttu-id="80008-122">Wenn Sie die [Kanonische PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md)entfernen möchten, sollten Sie auch die Kennzeichen **INSP_PROPDEFINITION** aus der [PidLidCustomFlag kanonische-Eigenschaft](pidlidcustomflag-canonical-property.md)entfernen.</span><span class="sxs-lookup"><span data-stu-id="80008-122">If you remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md), then you should also remove the **INSP_PROPDEFINITION** flag from the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md).</span></span>
  
<span data-ttu-id="80008-123">Die folgende Funktion, `RemoveOneOff`, akzeptiert als Eingabeparameter einen Zeiger auf eine Nachricht und ein Indikator, ob die [Kanonische PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md)zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="80008-123">The following function,  `RemoveOneOff`, accepts as input parameters a pointer to a message and an indicator whether to remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md).</span></span> <span data-ttu-id="80008-124">Verwenden den Nachrichtenzeiger, es ruft [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) , um die entsprechende Eigenschaft IDs erhalten und ruft dann [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) , um die benannten Eigenschaften zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="80008-124">Using the message pointer, it calls [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the appropriate property identifiers, and then calls [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) to remove the named properties.</span></span> <span data-ttu-id="80008-125">Außerdem ruft [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen der [PidLidCustomFlag kanonische-Eigenschaft](pidlidcustomflag-canonical-property.md) und löscht die **INSPIRON\_ONEOFFFLAGS** Flag und **INSP_PROPDEFINITION** Kennzeichnen von der Eigenschaft entsprechend also, Outlook 2010 und Outlook 2013 wird nicht für die benannten Eigenschaften gesucht, die entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="80008-125">It also calls [IMAPIProp::GetProps](imapiprop-getprops.md) to get the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md) and clears the **INSP\_ONEOFFFLAGS** flag and **INSP_PROPDEFINITION** flag as appropriate from that property, so that Outlook 2010 and Outlook 2013 will not look for those named properties that have been removed.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="80008-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80008-126">See also</span></span>

- [<span data-ttu-id="80008-127">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="80008-127">MAPI Constants</span></span>](mapi-constants.md)

