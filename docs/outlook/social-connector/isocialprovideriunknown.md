---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Stellt eine Instanz eines Outlook Social Connector (OSC)-Anbieters dar.
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285484"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Stellt eine Instanz eines Outlook Social Connector (OSC)-Anbieters dar.
  
## <a name="members"></a>Elemente

In der folgenden Tabelle sind die Member aufgeführt, die auf der **ISocialProvider** -Schnittstelle verfügbar sind. 
  
|**Name**|**Mitgliedstyp**|**Beschreibung**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |Eigenschaft  <br/> |Gibt ein Array von Zeichenfolgen zurück, die Website-URLs für den OSC-Anbieter angeben.  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |Methode  <br/> |Ruft eine automatisch konfigurierte [ISocialSession](isocialsessioniunknown.md)-Schnittstelle ab.  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die die Anbieter Funktionen beschreibt.  <br/> |
|[GetSession "](isocialprovider-getsession.md) <br/> |Methode  <br/> |Ruft eine [ISocialSession](isocialsessioniunknown.md) -Schnittstelle ab.  <br/> |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |Methode  <br/> |Diese Methode wird derzeit nicht unterstützt.  <br/> |
|[Load](isocialprovider-load.md) <br/> |Methode  <br/> |Initialisiert den OSC-Anbieter.  <br/> |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |Eigenschaft  <br/> |Gibt eine GUID, die einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.  <br/> |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |Eigenschaft  <br/> |Gibt ein Bytearray zurück, das das Symbol für das soziale Netzwerk darstellt.  <br/> |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge, die den Namen des sozialen Netzwerks darstellt.  <br/> |
|[Version](isocialprovider-version.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge, die die Versionsnummer des Anbieters für dieses soziale Netzwerk darstellt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein OSC-Anbieter muss diese Schnittstelle für die Kommunikation mit dem OSC implementieren.
  
## <a name="see-also"></a>Siehe auch

- [Outlook Social Connector-Anbieterschnittstellen](outlook-social-connector-provider-interfaces.md)

