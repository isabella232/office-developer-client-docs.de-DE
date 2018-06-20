---
title: Übermittlungsberichte Nachricht senden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d94785df9becf46bbfad66465facea35202c6079
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795491"
---
# <a name="sending-message-delivery-reports"></a>Übermittlungsberichte Nachricht senden

  
  
**Betrifft**: Outlook 
  
Einige zugrunde liegenden Messagingsysteme unterstützen Übermittlungsberichte und andere nicht. Wie der Adressbuchhierarchie bestimmt, ob Clientanwendungen Nachricht Übermittlung oder Nondelivery-Berichte gesendet werden können, ist Implementierungsdetail einzelnen Transport-Anbieter. Wenn Clientanwendungen Übermittlungsberichte gesendet werden können, mit Transportanbieter die [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) -Methode können um MAPI der erfolgreichen oder fehlgeschlagenen Lieferung für einen oder mehrere Empfänger zu informieren. MAPI generiert Übermittlung oder Nondelivery Berichte an diesen Empfänger entspricht. Transportanbieter können auch eingehende Übermittlung und Nondelivery Berichte, die systemeigene Nachrichtensystem in MAPI-Übermittlung sind und Unzustellbarkeitsberichten über **StatusRecips**übersetzen.
  

