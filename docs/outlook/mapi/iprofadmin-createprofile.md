---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a15561a6f3af35c1c7c2285bb6252e6400e0e8df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792751"
---
# <a name="iprofadmincreateprofile"></a>IProfAdmin::CreateProfile

  
  
**Betrifft**: Outlook 
  
Erstellt ein neues Profil.
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpszProfileName_
  
> [in] Ein Zeiger auf den Namen des neuen Profils.
    
 _lpszPassword_
  
> [in] Ein Zeiger auf das Kennwort für das neue Profil. 
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Profil erstellt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFAULT_SERVICES 
  
> MAPI sollte das neue Profil mit den Diensten Nachricht aufgefüllt, die in der die Datei "Mapisvc.inf" im Abschnitt [Default Services] enthalten sind.
    
MAPI_DIALOG 
  
> Konfigurationsblätter-Eigenschaft der einzelnen die Rollenanbieter in der Nachrichtendienste hinzugefügt werden soll, können angezeigt werden. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das neue Profil erstellt wurde.
    
MAPI_E_NO_ACCESS 
  
> Das angegebene neue Profil ist bereits vorhanden.
    
## <a name="remarks"></a>Hinweise

Die **IProfAdmin::CreateProfile** -Methode erstellt ein neues Profil. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **CreateProfile** bei der Installation oder können Sie jederzeit während einer Sitzung aufrufen. Bei der Installation diese Methode aufgerufen wird, werden viele der Konfigurationseinstellungen für die aus der Konfigurationsdatei Mapisvc.inf Vordergrund angezeigt. Wenn diese Methode während einer aktiven Sitzung aufgerufen wird, stammen die Einstellungen der Benutzer, der durch eine Reihe von Eigenschaftenseiten aufgefordert wird. 
  
Wenn das Flag MAPI_DEFAULT_SERVICES im _UlFlags_ -Parameter festgelegt ist, ruft **CreateProfile** die Nachricht Service Eintrag-Funktion für jeden Nachrichtendienst im Abschnitt [Default Services] in der Datei "Mapisvc.inf". Jede Nachricht Service Eintrag Point-Funktion wird mit der _UlContext_ -Parameter auf MSG_SERVICE_CREATE aufgerufen. 
  
Wenn die MAPI_DIALOG und die MAPI_DEFAULT_SERVICES Flags festgelegt sind, werden die Werte in den _UlUIParam_ und _UlFlags_ auch an die Nachricht Service Eintrag-Funktion übergeben. Die Nachricht Service Entry Point-Funktionen werden aufgerufen, nur, nachdem alle verfügbaren Informationen aus der Datei "Mapisvc.inf" auf das Profil hinzugefügt wurde. 
  
Der Name der dem neuen Profil und das zugehörige Kennwort kann bis zu 64 Zeichen lang sein und kann die folgenden Zeichen enthalten:
  
- Alle alphanumerischen Zeichen, einschließlich Akzent-Zeichen und das Unterstrichzeichen.
    
- Leerzeichen, jedoch nicht führende oder nachfolgende Leerzeichen.
    
Der Parameter _LpszPassword_ muss NULL oder einen Zeiger auf eine leere Zeichenfolge. 
  
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin: IUnknown](iprofadminiunknown.md)

