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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c744407790fecde6b6d89dff669ea4db07ce7701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791953"
---
# <a name="iabcontainerdeleteentries"></a>IABContainer::DeleteEntries

  
  
**Betrifft**: Outlook 
  
Entfernt einen oder mehrere Einträge in der Regel messaging Benutzern, Verteilerlisten oder andere Container.
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpEntries_
  
> [in] Ein Zeiger auf ein Array von [ENTRYLIST](entrylist.md) -Strukturen, die Eintragsbezeichner enthalten, die die zu löschenden Einträge darstellen. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die angegebenen Einträge wurden gelöscht. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber eine oder mehrere Einträge konnte nicht gelöscht werden. Wenn dieser Wert zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diesen Wert zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Abdlg.cpp  <br/> |CabDlg::OnDeleteSelectedItem  <br/> |MFCMAPI (engl.) wird die **DeleteEntries** -Methode verwendet, um einen bestimmten Eintrag aus einer Adressbuchcontainer zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

