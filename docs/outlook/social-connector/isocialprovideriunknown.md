---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Stellt eine Instanz eines Outlook Osc-Anbieters (Social Connector) dar.
ms.openlocfilehash: b784ce945988c983d28d93fd351bb2d10b4e48ec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583009"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Stellt eine Instanz eines Outlook Osc-Anbieters (Social Connector) dar.
  
## <a name="members"></a>Members

In der folgenden Tabelle sind die Elemente aufgeführt, die auf der **ISocialProvider-Schnittstelle** verfügbar sind. 
  
|**Name**|**Membertyp**|**Beschreibung**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |Eigenschaft  <br/> |Gibt ein Array von Zeichenfolgen zurück, die Website-URLs für den OSC-Anbieter angeben.  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |Methode  <br/> |Ruft eine automatisch konfigurierte [ISocialSession](isocialsessioniunknown.md)-Schnittstelle ab.  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die die Anbieterfunktionen beschreibt.  <br/> |
|[GetSession](isocialprovider-getsession.md) <br/> |Methode  <br/> |Ruft eine [ISocialSession-Schnittstelle](isocialsessioniunknown.md) ab.  <br/> |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |Methode  <br/> |Diese Methode wird derzeit nicht unterstützt.  <br/> |
|[Load](isocialprovider-load.md) <br/> |Methode  <br/> |Initialisiert den OSC-Anbieter.  <br/> |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |Eigenschaft  <br/> |Gibt eine GUID zurück, die einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.  <br/> |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |Eigenschaft  <br/> |Gibt ein Bytearray zurück, das das Symbol für das soziale Netzwerk darstellt.  <br/> |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge zurück, die den Namen des sozialen Netzwerks darstellt.  <br/> |
|[Version](isocialprovider-version.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge zurück, die die Versionsnummer des Anbieters für dieses soziale Netzwerk darstellt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Ein OSC-Anbieter muss diese Schnittstelle für die Kommunikation mit dem OSC implementieren.
  
## <a name="see-also"></a>Siehe auch

- [Outlook Anbieterschnittstellen für Connector für soziale Netzwerke](outlook-social-connector-provider-interfaces.md)

