---
title: Entwerfen einer Messagingdiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b572ebcec0a33d2134f4cf19b88e3132cbd47117
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582000"
---
# <a name="designing-a-message-service"></a>Entwerfen einer Messagingdiensts

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bevor Sie beginnen, dem Schreiben von Code, um Ihre Nachrichtendienst zu unterstützen, ist es wichtig, einen Entwurf erstellen. Beheben Sie die folgenden Probleme in Ihrer Entwurfsprozess:
  
1. Bestimmen Sie, wie viele Dienstanbieter in der Nachrichtendienst enthalten sein sollen. Enthalten Sie nur verwandte-Dienstanbieter (d. h., Providers, mit denen die selben Nachrichtensystem zusammenarbeiten) in Ihrem Dienst. Damit nicht zusammenhängenden-Dienstanbietern gehören nicht in der gleichen Message-Dienst. Verwenden Sie das Profil für die Integration von unabhängigen Dienstanbietern und Message-Dienste.
    
2. Bestimmen Sie, welche Art von Dienstanbietern in den Dienst enthalten sein sollen. Die meisten Messge Dienste enthalten einen Anbieter der einzelnen die Ressourcentypen. D. h., hat der normalen Messagingdiensts eine Adressbuchanbieter, eine Nachricht Speicheranbieter und eine Adressbuchhierarchie.
    
3. Bestimmen, wie viele DLLs sollte die Messagingdiensts enthalten. Die Anzahl von DLLs, die ein Nachrichtendienst verwendet hängt von folgendem ab:
    
   - Der Grad der Komplexität, die Sie als Writer des Diensts Nachricht bereit sind, zu behandeln sind.
    
   - Der Typ der Dienstanbieter in der Nachrichtendienst.
    
   - Die Beziehung, die der Dienst möglicherweise mit einem anderen Messagingdiensts muss.
    
   Da MAPI nur über einen Einstiegspunkt für jeden Anbietertyp speichert, nehmen Sie mehrere Anbieter des gleichen Typs nicht in einer einzigen DLL. Wenn es sinnvoll, mehrere Anbieter eines Typs enthalten ist, in separaten DLLs zu implementieren, oder haben sie eine Eintrag Funktion freizugeben. Eine andere Option besteht darin, implementieren Sie verwandte Message Dienste oder Message-Dienste, die die gleiche Installation verwenden können, und Konfigurationscode und Seitenverweisen auf dieselbe DLL zeigen-Funktion in einer DLL.
    
   Wenn möglich, ganz einfach, und verwenden Sie eine DLL, die die Implementierung der der Dienstanbieter in der Nachrichtendienst und der gesamte Code zum Installieren und Konfigurieren des Diensts Nachricht enthält. Wenn dies nicht möglich ist, können Sie eine DLL für die Installation und Konfiguration von Code und entweder eine einzelne DLL für alle-Dienstanbieter oder eine DLL für jeden Anbieter implementieren.
    
4. Bestimmen Sie einen Namen für den Dienst DLL oder DLLs. 
    
## <a name="see-also"></a>Siehe auch

- [Nachrichtendienstimplementierung](message-service-implementation.md)

