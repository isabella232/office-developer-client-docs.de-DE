---
title: Entfernen benutzerdefinierter Formulardefinitionen, die mit einer Nachricht gespeichert wurden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: ac162cb73cfdee83bf034de32064c5ed9df3bc02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345934"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a>Entfernen benutzerdefinierter Formulardefinitionen, die mit einer Nachricht gespeichert wurden
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird ein Codebeispiel in C++ gezeigt, das eine Nachricht, die mit einer benutzerdefinierten Formulardefinition gespeichert wurde, in einer regulären Nachricht ohne die Formulardefinition konvertiert.
  
In Microsoft Outlook 2010 oder Microsoft Outlook 2013 können Sie Formulare freigeben, die benutzerdefinierte Formularseiten enthalten, indem Sie Sie entweder in einer Formularbibliothek veröffentlichen oder die entsprechende Formulardefinition mit einer Nachricht speichern. Ein benutzerdefiniertes Formular, das mit einer Nachricht gespeichert wird, wird gemeinhin als "einmaliges Formular" bezeichnet, da das Formular nur zum Anzeigen dieser bestimmten Nachricht als einmalige Instanz freigegeben wird. Dies geschieht normalerweise, wenn das Formular nicht in einer Formularbibliothek veröffentlicht wird, aber der Empfänger das benutzerdefinierte Formular beim Öffnen des Elements verwenden soll. Sie können angeben, dass ein Formular im Formular-Designer eine einmalige Form ist, indem Sie das Kontrollkästchen **Formulardefinition mit Element senden** auf der **Eigenschaften** Seite des Formulars aktivieren. 
  
Formulare mit Formularseiten können mit Code in Visual Basic Scripting Edition (VBScript) angepasst werden. Nachrichten, die mit Formulardefinitionen gespeichert werden, sind in der Regel größer. Aus Sicherheits-und Speicher Gründen ignorieren Outlook 2010 und Outlook 2013 Formulardefinitionen, die mit einem beliebigen Element gespeichert werden.
  
Um eine Nachricht, die mit einer benutzerdefinierten Formulardefinition gespeichert wird, ohne zu konvertieren, müssen Sie vier benannte Eigenschaften entfernen:
  
- [Kanonische PidLidFormStorage-Eigenschaft](pidlidformstorage-canonical-property.md)
    
- [Kanonische PidLidPageDirStream-Eigenschaft](pidlidpagedirstream-canonical-property.md)
    
- [Kanonische PidLidFormPropStream-Eigenschaft](pidlidformpropstream-canonical-property.md)
    
- [Kanonische PidLidScriptStream-Eigenschaft](pidlidscriptstream-canonical-property.md)
    
Darüber hinaus sollten Sie auch die kanonische [Pidlidpropertydefinitionstream (-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) entfernen, die die Definitionen der benutzerdefinierten Eigenschaften enthält, die mit dieser Nachricht gespeichert wurden. Ein Nebeneffekt beim Entfernen dieser Eigenschaft ist, dass die Outlook 2010-oder Outlook 2013-Objektmodelle und die Outlook 2010-oder Outlook 2013-Benutzeroberfläche nicht mehr auf Benutzereigenschaften zugreifen können, die für die Nachricht festgelegt wurden. Sie können weiterhin über MAPI auf diese Eigenschaften und deren Werte zugreifen. Wenn Sie diese Eigenschaft nicht entfernen und die Nachricht mit einer anderen Formulardefinition gespeichert wird, wird die [kanonische Pidlidpropertydefinitionstream (-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) teilweise mit neuen Daten überschrieben, und die Datenintegrität wird nicht garantiert. 
  
Wenn Sie die [kanonische Pidlidpropertydefinitionstream (-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md)entfernen, sollten Sie auch das **INSP_PROPDEFINITION** -Flag aus der [kanonischen pidlidcustomflag (-Eigenschaft](pidlidcustomflag-canonical-property.md)entfernen.
  
Die folgende Funktion `RemoveOneOff`akzeptiert als Eingabeparameter einen Zeiger auf eine Nachricht und einen Indikator, ob die [kanonische pidlidpropertydefinitionstream (-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md)entfernt werden soll. Mithilfe des Nachrichten Zeigers wird [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) aufgerufen, um die entsprechenden Eigenschaftenbezeichner abzurufen, und dann wird [IMAPIProp::D eleteprops](imapiprop-deleteprops.md) aufgerufen, um die benannten Eigenschaften zu entfernen. Außerdem wird [IMAPIProp::](imapiprop-getprops.md) GetProps aufgerufen, um [die kanonische pidlidcustomflag (-Eigenschaft](pidlidcustomflag-canonical-property.md) zu erhalten und das **\_ONEOFFFLAGS** -Flag und das **INSP_PROPDEFINITION** -Flag gemäß dieser Eigenschaft zu löschen, sodass Outlook 2010 und Outlook 2013 sucht nicht nach diesen benannten Eigenschaften, die entfernt wurden. 
  
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

