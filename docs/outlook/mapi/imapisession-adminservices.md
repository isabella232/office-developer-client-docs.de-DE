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
ms.openlocfilehash: c639523a02047bf00c378dafd7bc698d7d4e5fff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405905"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen [IMsgServiceAdmin](imsgserviceadminiunknown.md) -Zeiger zurück, um Änderungen an den Nachrichtendiensten vorzunehmen. 
  
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
  
> Out Ein Zeiger auf einen Zeiger auf ein Nachrichtendienst-Verwaltungsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Ein Zeiger auf ein Nachrichtendienst-Verwaltungsobjekt wurde erfolgreich zurückgegeben.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **IMAPISession:: AdminServices** -Methode erstellt ein Nachrichtendienst-Verwaltungsobjekt, ein Objekt, das die **IMsgServiceAdmin** -Schnittstelle unterstützt und einen Zeiger zurückgibt. Mithilfe dieses Zeigers können Sie **IMsgServiceAdmin** -Methoden aufrufen, um einen beliebigen Nachrichtendienst im Sitzungsprofil zu ändern. Beachten Sie, dass diese Änderungen erst in der nächsten Sitzung wirksam werden. die aktuelle Sitzung ist nicht betroffen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIStoreFunctions. cpp  <br/> |GetServerName  <br/> |MFCMAPI verwendet die **IMAPISession:: AdminServices** -Methode, um auf das Profil zuzugreifen, um den Servernamen zu lesen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

