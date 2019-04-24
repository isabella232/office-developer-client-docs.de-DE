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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316723"
---
# <a name="designing-a-message-service"></a>Entwerfen eines Nachrichtendiensts

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor Sie mit dem Schreiben von Code beginnen, um den Nachrichtendienst zu unterstützen, ist es wichtig, einen Entwurf zu erstellen. Beheben Sie die folgenden Probleme in Ihrem Entwurfsprozess:
  
1. Legen Sie fest, wie viele Dienstanbieter in den Nachrichtendienst aufgenommen werden sollen. Schließen Sie nur Verwandte Dienstanbieter (also Anbieter, die mit demselben Messagingsystem arbeiten) in ihren Dienst ein. Nicht verwandte Dienstanbieter gehören nicht in den gleichen Nachrichtendienst. Verwenden Sie das Profil für die Integration nicht zusammenhängender Dienstanbieter und Nachrichtendienste.
    
2. Legen Sie fest, welche Art von Dienstanbietern in den Nachrichtendienst aufgenommen werden soll. Die meisten Messge-Dienste verfügen über einen Anbieter der einzelnen allgemeinen Typen. Das heißt, der typische Nachrichtendienst verfügt über einen Adressbuchanbieter, einen Nachrichtenspeicher Anbieter und einen Transportanbieter.
    
3. Bestimmen Sie, wie viele DLLs den Nachrichtendienst enthalten sollen. Die Anzahl der DLLs, die ein Nachrichtendienst verwendet, hängt von den folgenden:
    
   - Der Grad an Komplexität, den Sie als Verfasser des Nachrichtendiensts bereit sind.
    
   - Der Typ der Dienstanbieter im Nachrichtendienst.
    
   - Die Beziehung, die der Nachrichtendienst möglicherweise mit einem anderen Nachrichtendienst hat.
    
   Da MAPI nur einen Einstiegspunkt für jeden Anbietertyp speichert, dürfen Sie nicht mehrere Anbieter desselben Typs in eine einzelne DLL einbeziehen. Wenn es sinnvoll ist, mehrere Anbieter eines Typs einzuschließen, implementieren Sie Sie entweder in separaten DLLs, oder lassen Sie Sie eine Einstiegspunktfunktion freigeben. Eine weitere Option ist die Implementierung zugehöriger Nachrichtendienste oder Nachrichtendienste, die in der Lage sind, denselben Installations-und Konfigurationscode und dieselbe DLL-Einstiegspunktfunktion in einer DLL zu verwenden.
    
   Wenn möglich, halten Sie es einfach, und verwenden Sie eine DLL, die die Implementierung aller Dienstanbieter im Nachrichtendienst und den gesamten Code zum Installieren und Konfigurieren des Nachrichtendiensts enthält. Wenn dies nicht möglich ist, können Sie eine DLL für den Installations-und Konfigurationscode und entweder eine einzelne DLL für alle Dienstanbieter oder eine DLL für jeden Anbieter implementieren.
    
4. Bestimmen Sie einen Namen für die Nachrichtendienst-DLL oder DLLs. 
    
## <a name="see-also"></a>Siehe auch

- [Nachrichtendienst Implementierung](message-service-implementation.md)

