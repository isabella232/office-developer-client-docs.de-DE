---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Hinzufügen von Freunden, bei Bedarf oder Hybriden Synchronisierung von Freunden, bedarfsgesteuerten Synchronisierung von Aktivitäten oder im sozialen Netzwerk anmelden mit zwischengespeicherten Anmeldeinformationen unterstützt.
ms.openlocfilehash: b14804d35e54ebe9fe2a529fb2664f0a661653bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795999"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2: IUnknown

Hinzufügen von Freunden, bei Bedarf oder Hybriden Synchronisierung von Freunden, bedarfsgesteuerten Synchronisierung von Aktivitäten oder im sozialen Netzwerk anmelden mit zwischengespeicherten Anmeldeinformationen unterstützt.
  
## <a name="members"></a>Members

In der folgenden Tabelle werden die Member, die für die **ISocialSession2** -Schnittstelle verfügbar sind. 
  
|**Name**|**Typ des Elements**|**Beschreibung**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Methode  <br/> |Fügt die Person, die durch die Parameter _EmailAddresses_ und _DisplayName_ als einen Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert.  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge, die eine Sammlung von Aktivitäten, der durch den _HashedAddresses_ -Parameter angegebenen Benutzer darstellt.  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Methode  <br/> |Gibt eine Zeichenfolge, die eine Auflistung von Person und Teile des Bildes Details für die durch den _PersonsAddresses_ -Parameter angegebenen Benutzer enthält.  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Methode  <br/> |Meldet sich bei der social Network-Website mit zwischengespeicherten Anmeldeinformationen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Ein Anbieter Outlook Social Connector (OSC) können diese Schnittstelle implementieren, wenn der Anbieter unterstützt mit zwischengespeicherten Anmeldeinformationen auf Abruf oder Hybriden Synchronisierung von Freunden, bedarfsgesteuerten Synchronisierung von Aktivitäten oder im sozialen Netzwerk anmelden. Wenn der OSC-Anbieter **ISocialSession2** und unterstützt die folgenden Personen im sozialen Netzwerk implementiert, die OSC würde [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) anstelle von [ISocialSession::FollowPerson](isocialsession-followperson.md)aufrufen und der Anbieter implementiert werden müssen **ISocialSession2::FollowPersonEx**, sowie.
  
## <a name="see-also"></a>Siehe auch

- [Outlook Connector für soziale Netzwerke Provider-Schnittstellen](outlook-social-connector-provider-interfaces.md)

