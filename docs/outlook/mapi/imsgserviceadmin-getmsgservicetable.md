---
title: IMsgServiceAdminGetMsgServiceTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetMsgServiceTable
api_type:
- COM
ms.assetid: 064dd5ca-0108-4045-b17b-0bb29cb93346
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fcaebb96d4dca4e6bfbee7491dabeafcbd93a2eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410476"
---
# <a name="imsgserviceadmingetmsgservicetable"></a>IMsgServiceAdmin::GetMsgServiceTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf die Nachrichtendiensttabelle, eine Liste der Nachrichtendienste im Profil.
  
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
    
## <a name="remarks"></a>Hinweise

Die **IMsgServiceAdmin::GetMsgServiceTable-Methode** bietet Zugriff auf die Nachrichtendiensttabelle, eine Tabelle, die MAPI verwaltet, in der die aktuell im Sitzungsprofil installierten Nachrichtendienste aufgeführt sind. Eine vollständige Liste der Spalten in der Nachrichtendiensttabelle finden Sie unter [Message Service Table](message-service-tables.md).
  
Die Nachrichtendiensttabelle ist statisch. Nachdem einem Client Zugriff darauf gegeben wurde, wirken sich nachfolgende Nachrichtendienstergnungen oder -löschungen nicht auf ihn aus. Wenn im aktuellen Profil keine Nachrichtendienste vorhanden sind, gibt **GetMsgServiceTable** eine Tabelle mit null Zeilen zurück. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnRefreshView  <br/> |MFCMAPI verwendet die **IMsgServiceAdmin::GetMsgServiceTable-Methode,** um die Diensttabelle in ein Profil zu laden, das in der Ansicht gerendert werden soll.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

