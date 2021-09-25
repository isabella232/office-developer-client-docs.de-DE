---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9fa8107a551ed46d5b1790eb1965bf242cc79b2f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556322"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf die Profiltabelle, eine Tabelle, die Informationen zu allen verfügbaren Profilen enthält.
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Immer NULL.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die Profiltabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Profiltabelle wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IProfAdmin::GetProfileTable-Methode** ermöglicht den Zugriff auf die Profiltabelle, die eine Zeile für jedes verfügbare Profil enthält. Jede Zeile enthält nur zwei Spalten: den Anzeigenamen des Profils und ein Flag, das angibt, ob das Profil der Standardwert ist. 
  
Profile, die gelöscht wurden oder verwendet werden, aber für den Löschvorgang markiert wurden, sind nicht in der Profiltabelle enthalten. Die Profiltabelle ist statisch. Nachfolgende Hinzufügungen und Löschungen von Profilen werden in der Tabelle nicht widergespiegelt. 
  
Wenn keine Profile vorhanden sind, gibt **GetProfileTable** eine Tabelle mit null Zeilen zurück. 
  
Weitere Informationen zur Profiltabelle finden Sie unter [Profiltabellen.](profile-tables.md) 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnShowProfiles  <br/> |MFCMAPI verwendet die **IProfAdmin::GetProfileTable-Methode,** um die Profiltabelle abzurufen, die in einem neuen Dialogfeld angezeigt werden soll.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

