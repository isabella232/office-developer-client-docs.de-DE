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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407011"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

Stellt eine Person im sozialen Netzwerk dar.
  
## <a name="members"></a>Elemente

In der folgenden Tabelle sind die Elemente aufgeführt, die auf der **ISocialPerson-Schnittstelle verfügbar** sind. 
  
|**Name**|**Membertyp**|**Beschreibung**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |Methode  <br/> |Diese Methode ist seit dem Social Connector 2013 Outlook veraltet.  <br/> |
|[GetDetails](isocialperson-getdetails.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die Details für die Person darstellt, z. B. den Vornamen, den Nachnamen und eine URL zu einem Profilbild.  <br/> |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die eine Auflistung von Personen darstellt.  <br/> |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |Methode  <br/> |Diese Methode wird derzeit nicht unterstützt.  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Methode  <br/> |Ruft ein Array von Bytes ab, das die Bildressource für die Person enthält.  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Methode  <br/> |Diese Methode wird derzeit nicht unterstützt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Ein Outlook (Social Connector, OSC) muss diese Schnittstelle implementieren, um mit dem OSC zu kommunizieren.
  
## <a name="see-also"></a>Siehe auch

- [Outlook Schnittstellen für Anbieter für soziale Verbindungen](outlook-social-connector-provider-interfaces.md)

