---
title: IABContainerDeleteEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABContainer.DeleteEntries
api_type:
- COM
ms.assetid: 70a24811-0c41-4b44-8c63-7ef807bc9051
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 55938b7c002c974f5e06cd75205bbfbed986364e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610755"
---
# <a name="iabcontainerdeleteentries"></a>IABContainer::DeleteEntries

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Entfernt einen oder mehrere Einträge, in der Regel Messagingbenutzer, Verteilerlisten oder andere Container.
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpEntries_
  
> [in] Ein Zeiger auf ein Array von [ENTRYLIST-Strukturen,](entrylist.md) die Eintragsbezeichner enthalten, die die zu löschenden Einträge darstellen. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die angegebenen Einträge wurden erfolgreich gelöscht. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber mindestens einer der Einträge konnte nicht gelöscht werden. Wenn dieser Wert zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Um diesen Wert zu testen, verwenden Sie das **makro HR_FAILED.** Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Abdlg.cpp  <br/> |CabDlg::OnDeleteSelectedItem  <br/> |MFCMAPI verwendet die **DeleteEntries-Methode,** um einen bestimmten Eintrag aus einem Adressbuchcontainer zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

