---
title: Entfernen benutzerdefinierter Formulardefinitionen, die mit einer Nachricht gespeichert wurden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 737b04a8899a03931c98067909dce2ad2f47a339
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564274"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a>Entfernen benutzerdefinierter Formulardefinitionen, die mit einer Nachricht gespeichert wurden
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird ein Codebeispiel in C++ gezeigt, das eine Nachricht konvertiert, die mit einer benutzerdefinierten Formulardefinition in eine reguläre Nachricht ohne die Formulardefinition gespeichert wurde.
  
In Microsoft Outlook 2010 oder Microsoft Outlook 2013 können Sie Formulare freigeben, die benutzerdefinierte Formularseiten enthalten, indem Sie sie entweder in einer Formularbibliothek veröffentlichen oder die entsprechende Formulardefinition mit einer Nachricht speichern. Ein benutzerdefiniertes Formular, das mit einer Nachricht gespeichert wird, wird häufig als "einmaliges Formular" bezeichnet, da das Formular nur zum Anzeigen dieser bestimmten Nachricht als einmalige Instanz freigegeben wird. Dies geschieht in der Regel, wenn das Formular nicht in einer Formularbibliothek veröffentlicht wird, der Empfänger jedoch beim Öffnen des Elements das benutzerdefinierte Formular verwenden soll. Sie können festlegen, dass es sich bei einem Formular um ein einmaliges Formular im Formular-Designer handelt, indem Sie auf der **Eigenschaftenseite** des Formulars das Kontrollkästchen **Formulardefinition mit Element senden** aktivieren. 
  
Formulare, die Formularseiten enthalten, können mit Code in Visual Basic Scripting Edition (VBScript) angepasst werden. Nachrichten, die mit Formulardefinitionen gespeichert werden, sind in der Regel größer. Aus Sicherheits- und Speichergründen ignorieren Outlook 2010 und Outlook 2013 Formulardefinitionen, die mit einem beliebigen Element gespeichert wurden.
  
Um eine Nachricht zu konvertieren, die mit einer benutzerdefinierten Formulardefinition gespeichert wird, müssen Sie vier benannte Eigenschaften entfernen:
  
- [Kanonische PidLidFormStorage-Eigenschaft](pidlidformstorage-canonical-property.md)
    
- [Kanonische PidLidPageDirStream-Eigenschaft](pidlidpagedirstream-canonical-property.md)
    
- [Kanonische PidLidFormPropStream-Eigenschaft](pidlidformpropstream-canonical-property.md)
    
- [Kanonische PidLidScriptStream-Eigenschaft](pidlidscriptstream-canonical-property.md)
    
Darüber hinaus sollten Sie auch die [kanonische PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) entfernen, die die Definitionen der mit dieser Nachricht gespeicherten benutzerdefinierten Eigenschaften enthält. Ein Nebeneffekt des Entfernens dieser Eigenschaft besteht darin, dass die Outlook 2010- oder Outlook 2013-Objektmodelle und die Benutzeroberfläche Outlook 2010 oder Outlook 2013 nicht mehr auf Benutzereigenschaften zugreifen können, die für die Nachricht festgelegt wurden. Sie können weiterhin über MAPI auf diese Eigenschaften und deren Werte zugreifen. Wenn Sie diese Eigenschaft nicht entfernen und die Nachricht mit einer anderen Formulardefinition gespeichert wird, wird die [kanonische PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) teilweise mit neuen Daten überschrieben, und die Datenintegrität ist nicht gewährleistet. 
  
Wenn Sie die [kanonische PidLidPropertyDefinitionStream -Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md)entfernen, sollten Sie auch das **INSP_PROPDEFINITION** Flag aus der [kanonischen PidLidCustomFlag -Eigenschaft](pidlidcustomflag-canonical-property.md)entfernen.
  
Die folgende Funktion akzeptiert  `RemoveOneOff` als Eingabeparameter einen Zeiger auf eine Nachricht und einen Indikator, ob die [kanonische PidLidPropertyDefinitionStream -Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md)entfernt werden soll. Mithilfe des Nachrichtenzeigers ruft er [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) auf, um die entsprechenden Eigenschaftenbezeichner abzurufen, und ruft dann [IMAPIProp::D eleteProps](imapiprop-deleteprops.md) auf, um die benannten Eigenschaften zu entfernen. Es ruft auch [IMAPIProp::GetProps](imapiprop-getprops.md) auf, um die [kanonische PidLidCustomFlag-Eigenschaft](pidlidcustomflag-canonical-property.md) abzurufen, und löscht das **INSP \_ ONEOFFFLAGS-Flag** und **INSP_PROPDEFINITION** Flag entsprechend aus dieser Eigenschaft, sodass Outlook 2010 und Outlook 2013 nicht nach den benannten Eigenschaften suchen, die entfernt wurden. 
  
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

