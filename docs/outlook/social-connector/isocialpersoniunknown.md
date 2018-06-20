---
title: ISocialPerson IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a2fa12-a7ef-4a95-9875-72ec6f8ceac9
description: Stellt eine Person im sozialen Netzwerk.
ms.openlocfilehash: d6fca18ac2d2074239bd8b435bcd40971de83670
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795973"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson: IUnknown

Stellt eine Person im sozialen Netzwerk.
  
## <a name="members"></a>Members

In der folgenden Tabelle werden die Member, die für die **ISocialPerson** -Schnittstelle verfügbar sind. 
  
|**Name**|**Typ des Elements**|**Beschreibung**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |Methode  <br/> |Diese Methode ist seit Outlook Social Connector 2013 veraltet.  <br/> |
|[GetDetails](isocialperson-getdetails.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge, die Details zu einem Profilbild der Person ein, beispielsweise den Vornamen, Nachnamen sowie eine URL darstellt.  <br/> |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge, die eine Auflistung von Personen darstellt.  <br/> |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |Methode  <br/> |Diese Methode wird derzeit nicht unterstützt.  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Methode  <br/> |Ruft ein Array von Bytes, die die Bildressource der Person enthält.  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Methode  <br/> |Diese Methode wird derzeit nicht unterstützt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Ein Outlook Social Connector (OSC)-Anbieter muss diese Schnittstelle für die Kommunikation mit dem OSC implementieren.
  
## <a name="see-also"></a>Siehe auch

- [Outlook Connector für soziale Netzwerke Provider-Schnittstellen](outlook-social-connector-provider-interfaces.md)

