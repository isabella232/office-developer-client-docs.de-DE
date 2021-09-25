---
title: Entwerfen eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4b100f3daf901bf72cf9998b8678ad597646ef73
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584619"
---
# <a name="designing-a-message-service"></a>Entwerfen eines Nachrichtendiensts

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor Sie mit dem Schreiben von Code zur Unterstützung Ihres Nachrichtendiensts beginnen, ist es wichtig, ein Design zu erstellen. Beheben Sie die folgenden Probleme in Ihrem Entwurfsprozess:
  
1. Bestimmen Sie, wie viele Dienstanbieter in den Nachrichtendienst einbezogen werden sollen. Schließen Sie nur verwandte Dienstanbieter (d. h. Anbieter, die mit demselben Messagingsystem arbeiten) in Ihren Dienst ein. Nicht verbundene Dienstanbieter gehören nicht zum gleichen Nachrichtendienst. Verwenden Sie das Profil zum Integrieren von nicht verbundenen Dienstanbietern und Nachrichtendiensten.
    
2. Bestimmen Sie, welche Art von Dienstanbietern im Nachrichtendienst enthalten sein soll. Die meisten Messge-Dienste enthalten einen Anbieter für jeden der gängigen Typen. Das heißt, der typische Nachrichtendienst verfügt über einen Adressbuchanbieter, einen Nachrichtenspeicheranbieter und einen Transportanbieter.
    
3. Bestimmen Sie, wie viele DLLs den Nachrichtendienst enthalten sollen. Die Anzahl der DLLs, die ein Nachrichtendienst verwendet, hängt von Folgendem ab:
    
   - Der Komplexitätsgrad, den Sie als Autor des Nachrichtendiensts behandeln möchten.
    
   - Der Typ der Dienstanbieter im Nachrichtendienst.
    
   - Die Beziehung, die der Nachrichtendienst möglicherweise mit einem anderen Nachrichtendienst hat.
    
   Da die MAPI nur einen Einstiegspunkt für jeden Anbietertyp speichert, schließen Sie nicht mehrere Anbieter desselben Typs in eine einzelne DLL ein. Wenn es sinnvoll ist, mehrere Anbieter eines Typs einzuschließen, implementieren Sie sie entweder in separaten DLLs, oder lassen Sie sie eine Einstiegspunktfunktion freigeben. Eine weitere Möglichkeit besteht darin, verwandte Nachrichtendienste oder Nachrichtendienste zu implementieren, die den gleichen Installations- und Konfigurationscode und die gleiche DLL-Einstiegspunktfunktion in einer DLL verwenden können.
    
   Halten Sie es nach Möglichkeit einfach, und verwenden Sie eine DLL, die die Implementierung aller Dienstanbieter im Nachrichtendienst und den gesamten Code zum Installieren und Konfigurieren des Nachrichtendiensts enthält. Wenn dies nicht möglich ist, können Sie eine DLL für den Installations- und Konfigurationscode und entweder eine einzelne DLL für alle Dienstanbieter oder eine DLL für jeden Anbieter implementieren.
    
4. Ermitteln Sie einen Namen für die Nachrichtendienst-DLL oder -DLLs. 
    
## <a name="see-also"></a>Siehe auch

- [Message Service-Implementierung](message-service-implementation.md)

