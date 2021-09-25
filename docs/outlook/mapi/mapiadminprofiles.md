---
title: MAPIAdminProfiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c2ff33145b5a1358f12cbccebc79a60a96953d32
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584088"
---
# <a name="mapiadminprofiles"></a>MAPIAdminProfiles

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt ein Profilverwaltungsobjekt. 
  
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
  
> [in] Bitmaske mit Flags, die Optionen für die Diensteintragsfunktion angeben. 
    
 _lppProfAdmin_
  
> [out] Zeiger auf einen Zeiger auf das neue Profilverwaltungsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetProfAdmin  <br/> |MFCMAPI verwendet die **MAPIAdminProfiles-Methode,** um das Profilverwaltungsobjekt abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IProfAdmin::CreateProfile](iprofadmin-createprofile.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

