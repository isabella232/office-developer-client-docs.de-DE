---
title: IMAPISessionAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.AdminServices
api_type:
- COM
ms.assetid: 487fab39-5c2c-4e1a-9f90-4da64f5e198b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cb7fa7bb7dc17a89fc7cc40ae370accc40fa3941
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579839"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeiger [IMsgServiceAdmin](imsgserviceadminiunknown.md) für die Änderung Message-Dienste. 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lppServiceAdmin_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Objekt "Message" Service-Verwaltung.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Ein Zeiger auf ein Objekt "Message" Service Administration wurde erfolgreich zurückgegeben.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **IMAPISession::AdminServices** -Methode erstellt ein Service Administration Meldungsobjekt, ein Objekt, das die **IMsgServiceAdmin** -Schnittstelle unterstützt und gibt einen Zeiger zurück. Rufen Sie mithilfe dieser Zeiger **IMsgServiceAdmin** -Methoden, um die Nachrichtendienste im Profil der Sitzung zu ändern. Beachten Sie, dass diese Änderungen nicht übernommen, bis der nächste Sitzung werden; die aktuelle Sitzung ist nicht betroffen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |GetServerName  <br/> |MFCMAPI (engl.) wird die **IMAPISession::AdminServices** -Methode verwendet, Zugriff auf das Profil, um den Namen des Servers zu lesen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

