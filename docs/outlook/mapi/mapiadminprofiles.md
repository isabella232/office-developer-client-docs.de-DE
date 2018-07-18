---
title: MAPIAdminProfiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3cd1a19b23a3c4d3ff8a297881eb2b959585eb17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793119"
---
# <a name="mapiadminprofiles"></a>MAPIAdminProfiles

  
  
**Betrifft**: Outlook 
  
Erstellt ein Profil Administration-Objekt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Bitmaske aus Flags, die Optionen für die Funktion Eintrag angibt. 
    
 _lppProfAdmin_
  
> [out] Zeiger auf einen Zeiger auf das neue Profil Administration-Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetProfAdmin  <br/> |MFCMAPI (engl.) verwendet die **"MAPIAdminProfiles"** -Methode, um das Profil Administration-Objekt abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IProfAdmin::CreateProfile](iprofadmin-createprofile.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

