---
title: ISocialPerson IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a2fa12-a7ef-4a95-9875-72ec6f8ceac9
description: Stellt eine Person im sozialen Netzwerk dar.
ms.openlocfilehash: 0ad129b0fc15fc9f3ccdf1cff7d8519bb07b024e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331941"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

Stellt eine Person im sozialen Netzwerk dar.
  
## <a name="members"></a>Elemente

In der folgenden Tabelle sind die Member aufgeführt, die auf der **ISocialPerson** -Schnittstelle verfügbar sind. 
  
|**Name**|**Mitgliedstyp**|**Beschreibung**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |Methode  <br/> |Diese Methode ist seit Outlook Social Connector 2013 veraltet.  <br/> |
|[GetDetails](isocialperson-getdetails.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die Details für die Person darstellt, wie den Vornamen, den Nachnamen und eine URL zu einem Profilbild.  <br/> |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die eine Auflistung von Personen darstellt.  <br/> |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |Methode  <br/> |Diese Methode wird derzeit nicht unterstützt.  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Methode  <br/> |Ruft ein Bytearray ab, das die Bildressource für die Person enthält.  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Methode  <br/> |Diese Methode wird derzeit nicht unterstützt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein Outlook Social Connector-Anbieter (OSC) muss diese Schnittstelle für die Kommunikation mit dem OSC implementieren.
  
## <a name="see-also"></a>Siehe auch

- [Outlook Social Connector-Anbieterschnittstellen](outlook-social-connector-provider-interfaces.md)

