---
title: IABContainerDeleteEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.DeleteEntries
api_type:
- COM
ms.assetid: 70a24811-0c41-4b44-8c63-7ef807bc9051
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e3b238129e55e03da33ef3af75ecce7e73fbad03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425596"
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
  
> in Ein Zeiger auf ein Array von [entrylist](entrylist.md) -Strukturen, die Eintrags-IDs enthalten, die die zu löschenden Einträge darstellen. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die angegebenen Einträge wurden erfolgreich gelöscht. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber mindestens einer der Einträge konnte nicht gelöscht werden. Wenn dieser Wert zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das **HR_FAILED** -Makro, um diesen Wert zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Abdlg. cpp  <br/> |CabDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI verwendet die **DeleteEntries** -Methode, um einen bestimmten Eintrag aus einem Adressbuchcontainer zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

