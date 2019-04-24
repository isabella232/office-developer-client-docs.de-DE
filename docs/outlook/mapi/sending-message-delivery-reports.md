---
title: Senden von nachrichtenÜbermittlungsBerichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2a31e7d088d5c1f94b272cb4d307f3aff99f32ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332837"
---
# <a name="sending-message-delivery-reports"></a>Senden von nachrichtenÜbermittlungsBerichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige zugrunde liegende Messagingsysteme unterstützen Übermittlungsberichte und andere nicht. Wie der Transportanbieter bestimmt, ob Nachrichtenübermittlungs-oder Unzustellbarkeitsberichte an Clientanwendungen gesendet werden können, ist ein Implementierungsdetail für einzelne Transportanbieter. Wenn Übermittlungsberichte an Clientanwendungen gesendet werden können, verwenden Transportanbieter die [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) -Methode, um MAPI über eine erfolgreiche oder nicht erfolgreiche Übermittlung für einen oder mehrere Empfänger zu benachrichtigen. MAPI generiert dann Zusteller-oder Unzustellbarkeitsberichte, die diesen Empfängern entsprechen. Transport Anbieter können auch eingehende und nicht zugestellte Berichte, die im Messagingsystem nativ sind, über **StatusRecips**in MAPI-Übermittlungs-und Unzustellbarkeitsberichte übersetzen.
  

