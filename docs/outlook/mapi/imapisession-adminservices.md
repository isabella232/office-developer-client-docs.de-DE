---
title: IMAPISessionAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.AdminServices
api_type:
- COM
ms.assetid: 487fab39-5c2c-4e1a-9f90-4da64f5e198b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c39051ed0a3b112293d3e851883d233c15a2b277
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625525"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen [IMsgServiceAdmin-Zeiger](imsgserviceadminiunknown.md) zum Vornehmen von Änderungen an Nachrichtendiensten zurück. 
  
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
  
> [out] Ein Zeiger auf einen Zeiger auf ein Nachrichtendienst-Verwaltungsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Ein Zeiger auf ein Nachrichtendienst-Verwaltungsobjekt wurde erfolgreich zurückgegeben.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **IMAPISession::AdminServices-Methode** erstellt ein Nachrichtendienst-Verwaltungsobjekt, ein Objekt, das die **IMsgServiceAdmin-Schnittstelle** unterstützt und einen Zeiger zurückgibt. Mit diesem Zeiger können Sie **IMsgServiceAdmin-Methoden** aufrufen, um einen der Nachrichtendienste im Sitzungsprofil zu ändern. Beachten Sie, dass diese Änderungen erst in der nächsten Sitzung wirksam werden. Die aktuelle Sitzung ist davon nicht betroffen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |GetServerName  <br/> |MFCMAPI verwendet die **IMAPISession::AdminServices-Methode,** um auf das Profil zuzugreifen, um den Servernamen zu lesen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

