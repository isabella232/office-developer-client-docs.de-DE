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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409958"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Stellt eine Instanz eines Outlook Social Connector (OSC)-Anbieters dar.
  
## <a name="members"></a>Elemente

In der folgenden Tabelle sind die Elemente aufgeführt, die auf der **ISocialProvider-Schnittstelle verfügbar** sind. 
  
|**Name**|**Membertyp**|**Beschreibung**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |Eigenschaft  <br/> |Gibt ein Array von Zeichenfolgen zurück, die Website-URLs für den OSC-Anbieter angeben.  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |Methode  <br/> |Ruft eine automatisch konfigurierte [ISocialSession](isocialsessioniunknown.md)-Schnittstelle ab.  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die Anbieterfunktionen beschreibt.  <br/> |
|[GetSession](isocialprovider-getsession.md) <br/> |Methode  <br/> |Ruft eine [ISocialSession-Schnittstelle](isocialsessioniunknown.md) ab.  <br/> |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |Methode  <br/> |Diese Methode wird derzeit nicht unterstützt.  <br/> |
|[Load](isocialprovider-load.md) <br/> |Methode  <br/> |Initialisiert den OSC-Anbieter.  <br/> |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |Eigenschaft  <br/> |Gibt eine GUID zurück, die einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.  <br/> |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |Eigenschaft  <br/> |Gibt ein Array von Bytes zurück, das das Symbol für das soziale Netzwerk darstellt.  <br/> |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge zurück, die den Namen des sozialen Netzwerks darstellt.  <br/> |
|[Version](isocialprovider-version.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge zurück, die die Versionsnummer des Anbieters für dieses soziale Netzwerk darstellt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Ein OSC-Anbieter muss diese Schnittstelle implementieren, um mit dem OSC zu kommunizieren.
  
## <a name="see-also"></a>Siehe auch

- [Outlook Social Connector Provider Interfaces](outlook-social-connector-provider-interfaces.md)

