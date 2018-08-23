---
title: Senden von Nachrichtenübermittlungsberichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 717494f30fd4d43e94a7c6a37770e2eab8ebb59e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593599"
---
# <a name="sending-message-delivery-reports"></a>Senden von Nachrichtenübermittlungsberichten

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Einige zugrunde liegenden Messagingsysteme unterstützen Übermittlungsberichte und andere nicht. Wie der Adressbuchhierarchie bestimmt, ob Clientanwendungen Nachricht Übermittlung oder Nondelivery-Berichte gesendet werden können, ist Implementierungsdetail einzelnen Transport-Anbieter. Wenn Clientanwendungen Übermittlungsberichte gesendet werden können, mit Transportanbieter die [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) -Methode können um MAPI der erfolgreichen oder fehlgeschlagenen Lieferung für einen oder mehrere Empfänger zu informieren. MAPI generiert Übermittlung oder Nondelivery Berichte an diesen Empfänger entspricht. Transportanbieter können auch eingehende Übermittlung und Nondelivery Berichte, die systemeigene Nachrichtensystem in MAPI-Übermittlung sind und Unzustellbarkeitsberichten über **StatusRecips**übersetzen.
  

