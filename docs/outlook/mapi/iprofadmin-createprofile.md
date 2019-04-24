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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b104c62eb617e6c68f85dea4ef6379c831733844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317115"
---
# <a name="iprofadmincreateprofile"></a>IProfAdmin::CreateProfile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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
  
> in Ein Zeiger auf den Namen des neuen Profils.
    
 _lpszPassword_
  
> in Ein Zeiger auf das Kennwort des neuen Profils. 
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster aller von dieser Methode angezeigten Dialogfelder oder Fenster.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Erstellung des Profils steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFAULT_SERVICES 
  
> MAPI sollte das neue Profil mit den Nachrichtendiensten auffüllen, die im Abschnitt [Default Services] der Datei MAPISVC. inf enthalten sind.
    
MAPI_DIALOG 
  
> Die Konfigurationseigenschaften Blätter der einzelnen Anbieter in den Nachrichtendiensten, die hinzugefügt werden sollen, können angezeigt werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das neue Profil wurde erstellt.
    
MAPI_E_NO_ACCESS 
  
> Das angegebene neue Profil ist bereits vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Die **IProfAdmin::** CreateProfile-Methode erstellt ein neues Profil. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können **CreateProfile** während der Anwendungsinstallation oder zu einem beliebigen Zeitpunkt während einer Sitzung aufrufen. Wenn diese Methode zur Installation aufgerufen wird, stammen viele Konfigurationseinstellungen aus der Konfigurationsdatei MAPISVC. inf. Wenn diese Methode während einer aktiven Sitzung aufgerufen wird, stammen die Einstellungen vom Benutzer, der durch eine Reihe von Eigenschaftenblättern dazu aufgefordert wird. 
  
Wenn das MAPI_DEFAULT_SERVICES-Flag im Parameter _ulFlags_ festgelegt ist, ruft CreateProfile die Entry Point-Funktion des Nachrichtendiensts für jeden Nachrichtendienst im Abschnitt [Default Services] in der Datei MAPISVC. inf auf. **** Jede Nachrichtendienst-Einstiegspunktfunktion wird aufgerufen, wobei der _ulContext_ -Parameter auf MSG_SERVICE_CREATE festgelegt ist. 
  
Wenn sowohl die MAPI_DIALOG-als auch die MAPI_DEFAULT_SERVICES-Flags festgelegt werden, werden die Werte in den Parametern _ulUIParam_ und _ulFlags_ ebenfalls an die Einstiegspunktfunktion des Nachrichtendiensts übergeben. Die Nachrichtendienst-Einstiegspunktfunktionen werden nur aufgerufen, nachdem dem Profil alle verfügbaren Informationen aus der Datei MAPISVC. inf hinzugefügt wurden. 
  
Der Name des neuen Profils und sein Kennwort können bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:
  
- Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und der Unterstrich.
    
- Eingebettete Leerzeichen, aber keine führenden oder nachstehenden Leerzeichen.
    
Der _lpszPassword_ -Parameter muss NULL oder ein Zeiger auf eine leere Zeichenfolge sein. 
  
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

