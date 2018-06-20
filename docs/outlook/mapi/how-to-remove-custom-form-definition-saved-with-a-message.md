---
title: Entfernen Sie benutzerdefinierter Formulardefinition gespeichert mit einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 9581656c40af39338f8919903f6d0de29c20a061
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791877"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a>Entfernen Sie benutzerdefinierter Formulardefinition gespeichert mit einer Nachricht
  
**Betrifft**: Outlook 
  
In diesem Thema wird ein Codebeispiel in C++, die eine Nachricht konvertiert, die mit der Definition für ein benutzerdefiniertes Formular auf eine reguläre Nachricht ohne die Formulardefinition gespeichert wurde.
  
In Microsoft Outlook 2010 oder Microsoft Outlook 2013 können Sie Formulare mit benutzerdefinierten Formularseiten in einer Formularbibliothek veröffentlichen, oder speichern die entsprechenden Formulardefinition mit einer Nachricht freigeben. Ein benutzerdefiniertes Formular mit einer Nachricht gespeichert wird häufig als "einmaliges Formular," bezeichnet, da das Formular gemeinsam genutzt wird nur für die betreffende Nachricht als einmaligen Instanz anzeigen. Sie dies in der Regel das Formular wird nicht in einer Formularbibliothek veröffentlicht, aber den Empfänger das benutzerdefinierte Formular beim Öffnen des Elements verwendet werden soll. Sie können angeben, dass ein Formular einer einmaligen im Formular-Designer ist, indem Sie das Kontrollkästchen **Element mit Beschreibung senden** auf der Seite **Eigenschaften** des Formulars auswählen. 
  
Formularen mit Formularseiten können mit Code in Visual Basic Scripting Edition (VBScript) angepasst werden. Nachrichten, die mit Formulardefinitionen gespeichert sind sind im Allgemeinen größer Größe. Ignorieren für Sicherheit und Storage Gründe Outlook 2010 und Outlook 2013 Formulardefinitionen mit beliebigen Elements gespeichert.
  
Um eine Nachricht zu konvertieren, die mit der Definition für ein benutzerdefiniertes Formular auf eine ohne gespeichert wird, müssen Sie vier benannte Eigenschaften entfernen:
  
- [Kanonische PidLidFormStorage-Eigenschaft](pidlidformstorage-canonical-property.md)
    
- [Kanonische PidLidPageDirStream-Eigenschaft](pidlidpagedirstream-canonical-property.md)
    
- [Kanonische PidLidFormPropStream-Eigenschaft](pidlidformpropstream-canonical-property.md)
    
- [Kanonische PidLidScriptStream-Eigenschaft](pidlidscriptstream-canonical-property.md)
    
Darüber hinaus sollten Sie auch die [PidLidPropertyDefinitionStream kanonische-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) entfernen, die enthält die Definitionen der benutzerdefinierten Eigenschaften, die mit dieser Nachricht gespeichert wurden. Eine Auswirkung dieser Eigenschaft entfernen, die die Objektmodelle von Outlook 2010 oder Outlook 2013 ist und die Benutzeroberfläche von Outlook 2010 oder Outlook 2013 werden nicht mehr Benutzer Eigenschaften zugreifen, die für die Nachricht festgelegt wurden. Sie können weiterhin auf diese Eigenschaften und deren Werte durch MAPI zuzugreifen. Beachten Sie, dass wenn diese Eigenschaft nicht entfernt und die Nachricht mit einem anderen Formulardefinition gespeichert ist, wird die [Kanonische PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) teilweise mit neuen Daten überschrieben und Datenintegrität nicht unbedingt. 
  
Wenn Sie die [Kanonische PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md)entfernen möchten, sollten Sie auch die Kennzeichen **INSP_PROPDEFINITION** aus der [PidLidCustomFlag kanonische-Eigenschaft](pidlidcustomflag-canonical-property.md)entfernen.
  
Die folgende Funktion, `RemoveOneOff`, akzeptiert als Eingabeparameter einen Zeiger auf eine Nachricht und ein Indikator, ob die [Kanonische PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md)zu entfernen. Verwenden den Nachrichtenzeiger, es ruft [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) , um die entsprechende Eigenschaft IDs erhalten und ruft dann [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) , um die benannten Eigenschaften zu entfernen. Außerdem ruft [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen der [PidLidCustomFlag kanonische-Eigenschaft](pidlidcustomflag-canonical-property.md) und löscht die **INSPIRON\_ONEOFFFLAGS** Flag und **INSP_PROPDEFINITION** Kennzeichnen von der Eigenschaft entsprechend also, Outlook 2010 und Outlook 2013 wird nicht für die benannten Eigenschaften gesucht, die entfernt wurden. 
  
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

## <a name="see-also"></a>Siehe auch

- [MAPI-Konstanten](mapi-constants.md)

