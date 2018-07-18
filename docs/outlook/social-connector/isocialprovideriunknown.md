---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Stellt eine Instanz eines Anbieters Outlook Social Connector (OSC).
ms.openlocfilehash: 912b2d92137febe80e0d97362e0a490f138b2e66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796102"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Stellt eine Instanz eines Anbieters Outlook Social Connector (OSC).
  
## <a name="members"></a>Elemente

In der folgenden Tabelle werden die Member, die für die **ISocialProvider** -Schnittstelle verfügbar sind. 
  
|**Name**|**Typ des Elements**|**Beschreibung**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |Eigenschaft  <br/> |Gibt ein Array von Zeichenfolgen, die Website-URLs für den OSC-Anbieter angeben.  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |Methode  <br/> |Ruft eine automatisch konfigurierte [ISocialSession](isocialsessioniunknown.md) -Schnittstelle.  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge, die vom Anbieterfunktionen beschreibt.  <br/> |
|[GetSession](isocialprovider-getsession.md) <br/> |Methode  <br/> |Ruft eine [ISocialSession](isocialsessioniunknown.md) -Schnittstelle.  <br/> |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |Methode  <br/> |Diese Methode wird derzeit nicht unterstützt.  <br/> |
|[Load](isocialprovider-load.md) <br/> |Methode  <br/> |Initialisiert den OSC-Anbieter.  <br/> |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |Eigenschaft  <br/> |Gibt eine GUID, die einen eindeutigen Bezeichner für das soziale Netzwerk darstellt.  <br/> |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |Eigenschaft  <br/> |Gibt ein Array von Bytes, die das Symbol für das soziale Netzwerk darstellt.  <br/> |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge, die den Namen für soziale Netzwerke darstellt.  <br/> |
|[Version](isocialprovider-version.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge, die die Versionsnummer des Anbieters für diese für soziale Netzwerke darstellt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein OSC-Anbieter muss diese Schnittstelle für die Kommunikation mit dem OSC implementieren.
  
## <a name="see-also"></a>Siehe auch

- [Outlook Connector für soziale Netzwerke Provider-Schnittstellen](outlook-social-connector-provider-interfaces.md)

