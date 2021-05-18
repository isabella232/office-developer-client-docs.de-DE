---
title: Entwerfen eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 19a8a939685c440901f3f57d72baf673a579e590
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404295"
---
# <a name="designing-a-message-service"></a>Entwerfen eines Nachrichtendiensts

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor Sie mit dem Schreiben von Code zur Unterstützung Ihres Nachrichtendiensts beginnen, ist es wichtig, einen Entwurf zu erstellen. Beheben Sie die folgenden Probleme in Ihrem Entwurfsprozess:
  
1. Bestimmen Sie, wie viele Dienstanbieter in den Nachrichtendienst einbezogen werden sollen. Schließen Sie nur verwandte Dienstanbieter (d. h. Anbieter, die mit demselben Messagingsystem arbeiten) in Ihren Dienst ein. Nicht verwandte Dienstanbieter gehören nicht zum gleichen Nachrichtendienst. Verwenden Sie das Profil zum Integrieren nicht verwandter Dienstanbieter und Nachrichtendienste.
    
2. Bestimmen Sie, welcher Typ von Dienstanbietern in den Nachrichtendienst einbezogen werden soll. Die meisten Messgedienste enthalten einen Anbieter für jeden der gängigen Typen. Das heißt, der typische Nachrichtendienst verfügt über einen Adressbuchanbieter, einen Nachrichtenspeicheranbieter und einen Transportanbieter.
    
3. Bestimmen Sie, wie viele DLLs den Nachrichtendienst enthalten sollen. Die Anzahl der dlLs, die ein Nachrichtendienst verwendet, hängt von folgenden Kriterien ab:
    
   - Der Komplexitätsgrad, den Sie als Verfasser des Nachrichtendiensts verarbeiten möchten.
    
   - Der Typ der Dienstanbieter im Nachrichtendienst.
    
   - Die Beziehung, die der Nachrichtendienst möglicherweise mit einem anderen Nachrichtendienst hat.
    
   Da MAPI nur einen Einstiegspunkt für jeden Anbietertyp speichert, schließen Sie nicht mehrere Anbieter desselben Typs in eine einzelne DLL ein. Wenn es sinnvoll ist, mehrere Anbieter eines Typs zu verwenden, implementieren Sie sie entweder in separaten DLLs, oder lassen Sie sie eine Einstiegspunktfunktion gemeinsam nutzen. Eine weitere Option besteht in der Implementierung verwandter Nachrichtendienste oder Nachrichtendienste, die denselben Installations- und Konfigurationscode und dieselbe DLL-Einstiegspunktfunktion in einer DLL verwenden können.
    
   Halten Sie es möglichst einfach, und verwenden Sie eine DLL, die die Implementierung aller Dienstanbieter im Nachrichtendienst und den ganzen Code zum Installieren und Konfigurieren des Nachrichtendiensts enthält. Wenn dies nicht möglich ist, können Sie eine DLL für den Installations- und Konfigurationscode und entweder eine einzelne DLL für alle Dienstanbieter oder eine DLL für jeden Anbieter implementieren.
    
4. Bestimmen Sie einen Namen für die Nachrichtendienst-DLL oder DLLs. 
    
## <a name="see-also"></a>Siehe auch

- [Implementierung des Nachrichtendiensts](message-service-implementation.md)

