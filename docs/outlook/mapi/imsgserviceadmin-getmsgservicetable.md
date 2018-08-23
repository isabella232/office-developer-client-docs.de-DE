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
ms.openlocfilehash: 5d8e91490cc39c3f259d35a923bb3bcbb2bf6011
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568168"
---
# <a name="imsgserviceadmingetmsgservicetable"></a>IMsgServiceAdmin::GetMsgServiceTable

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf die Nachricht Service Tabelle eine Liste der Nachrichtendienste im Profil.
  
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
  
> [out] Ein Zeiger auf einen Zeiger auf die Nachricht Service-Tabelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Tabelle der Dienste wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgServiceAdmin::GetMsgServiceTable** -Methode ermöglicht den Zugriff auf die Nachricht Service Tabelle eine Tabelle, die MAPI verwaltet, die Message-Dienste im Profil der Sitzung derzeit installiert aufgeführt. Eine vollständige Liste der Spalten in der Tabelle der Dienste finden Sie unter [Message Service-Tabelle](message-service-tables.md).
  
Die Tabelle der Dienste sind statisch. Nachdem ein Client Zugriff darauf gewährt wurde, wirkt nachfolgende Meldung Dienst hinzufügen oder Löschen nicht sich. Wenn keine Message-Dienste in das aktuelle Profil vorhanden sind, gibt **GetMsgServiceTable** eine Tabelle mit 0 (null) Zeilen zurück. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnRefreshView  <br/> |MFCMAPI (engl.) verwendet die **IMsgServiceAdmin::GetMsgServiceTable** -Methode zum Laden der Tabelle der Dienste in einem Profil in der Ansicht gerendert werden soll.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

