---
title: Schreiben eines automatisierten Clients
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eaa7e53902aa2a862c8f1ff279b05892ad891001
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619449"
---
# <a name="writing-an-automated-client"></a>Schreiben eines automatisierten Clients

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine automatisierte Clientanwendung ist eine Anwendung, die unbeaufsichtigt ausgeführt wird und keine Benutzeroberfläche anzeigt.
  
 Standardmäßig wird bei vielen MAPI-Schnittstellenmethoden eine Benutzeroberfläche angezeigt. Alle diese Methoden verfügen über Flags, mit denen ein Client diese Anzeige entweder zulassen oder unterdrücken kann. Obwohl die MAPI erwartet, dass Dienstanbieter diese Flags berücksichtigen, gibt es einige Anbieter, die diese Erwartungen nicht immer erfüllen. Ein berechtigter Grund dafür, die Flags nicht zu berücksichtigen, ist die Abhängigkeit des Dienstanbieters von einem anderen Dienst, der keine Unterdrückung der Benutzeroberfläche zulässt. Wenn Sie einen automatisierten Client entwickeln, achten Sie sorgfältig auf die von Ihnen verwendeten Dienstanbieter und deren Konfiguration. Gehen Sie nicht davon aus, dass alle Aufrufe zum Unterdrücken einer Benutzeroberfläche erfolgreich sind. 
  
Automatisierte Clients müssen über die erforderlichen Informationen für die ordnungsgemäße Konfiguration der einzelnen Nachrichtendienste im Profil verfügen. Es gibt zwei Möglichkeiten, Konfigurationsinformationen zur Anmeldezeit anzugeben:
  
- Der Dienstanbieter kann Informationen aus dem Profil abrufen.
    
- Der Dienstanbieter kann den Benutzer zur Eingabe von Informationen auffordern. 
    
Da die zweite Option für automatisierte Clients nicht verfügbar ist, müssen diese Clients die erste Option verwenden. Clients müssen ihre Profile sorgfältig konfigurieren, um sicherzustellen, dass diese Option immer funktioniert.
  
Automatisierte Clients legen immer das MAPI_NO_MAIL Flag im [MAPILogonEx-Funktionsaufruf](mapilogonex.md) fest, um eine MAPI-Sitzung zu starten. 
  

