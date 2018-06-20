---
title: Schreiben Sie einen automatisierten Client
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e5357c1e822dda35d3f38e00f91b58adbaf0ff9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795848"
---
# <a name="writing-an-automated-client"></a>Schreiben Sie einen automatisierten Client

  
  
**Betrifft**: Outlook 
  
Eine automatisierte Client-Anwendung ist eine Anwendung, die unbeaufsichtigte, ohne Benutzeroberfläche ausgeführt wird.
  
 Standardmäßig an vielen MAPI-Schnittstellenmethoden eine Benutzeroberfläche. Alle diese Methoden haben Flags, die einen Client zulassen oder unterdrückt diese Anzeige zulassen. Obwohl MAPI-Dienstanbieter diese Flags berücksichtigt erwartet, sind einige Anbieter, die diese Erwartungen nicht immer entsprechen. Ein legitimer Grund nicht berücksichtigt die Kennzeichen ist die Abhängigkeit des Dienstanbieters einer anderen Dienst, der keine Benutzer Schnittstelle Unterdrückung zulässt. Wenn Sie einen automatisierten Client entwickeln, achten Sie darauf achten auf der Dienstanbieter, die Sie verwenden und wie diese konfiguriert werden. Gehen Sie nicht, dass alle Ihre Anrufe an eine Benutzeroberfläche unterdrücken hergestellt werden kann. 
  
Automatisierte Clients benötigen in das Profil die erforderliche Informationen für die ordnungsgemäße Konfiguration der einzelnen Message-Dienste zur Verfügung. Es gibt zwei Methoden, um Konfigurationsinformationen bei der Anmeldung angeben:
  
- Der Dienstanbieter kann Informationen aus dem Profil abrufen.
    
- Der Dienstanbieter kann der Benutzer Informationen aufgefordert. 
    
Da die zweite Option für automatisierte Clients als nicht verfügbar ist, müssen diese Clients die erste Option verwenden. Clients müssen ihre Profile sorgfältig durch, um sicherzustellen, dass diese Option immer konfigurieren.
  
Automatisierte Clients legen Sie das MAPI_NO_MAIL-Flag immer im Funktionsaufruf [MAPILogonEx](mapilogonex.md) um einen MAPI-Sitzung zu starten. 
  

