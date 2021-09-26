---
title: IMsgServiceAdminGetMsgServiceTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.GetMsgServiceTable
api_type:
- COM
ms.assetid: 064dd5ca-0108-4045-b17b-0bb29cb93346
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 368c32374e47dd97dce54980c566ac14f78c75ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620716"
---
# <a name="imsgserviceadmingetmsgservicetable"></a>IMsgServiceAdmin::GetMsgServiceTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf die Nachrichtendiensttabelle, eine Liste der Nachrichtendienste im Profil.
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Immer NULL.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die Nachrichtendiensttabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachrichtendiensttabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgServiceAdmin::GetMsgServiceTable-Methode** ermöglicht den Zugriff auf die Nachrichtendiensttabelle, eine Tabelle, die MAPI verwaltet, in der die derzeit im Sitzungsprofil installierten Nachrichtendienste aufgeführt sind. Eine vollständige Liste der Spalten in der Nachrichtendiensttabelle finden Sie unter [Message Service Table](message-service-tables.md).
  
Die Nachrichtendiensttabelle ist statisch. Nachdem ein Client Zugriff darauf erhalten hat, wirken sich nachfolgende Hinzufügungen oder Löschungen des Nachrichtendiensts nicht darauf aus. Wenn im aktuellen Profil keine Nachrichtendienste vorhanden sind, gibt **GetMsgServiceTable** eine Tabelle mit null Zeilen zurück. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnRefreshView  <br/> |MFCMAPI verwendet die **IMsgServiceAdmin::GetMsgServiceTable-Methode,** um die Diensttabelle in einem Profil zu laden, das in der Ansicht gerendert werden soll.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

