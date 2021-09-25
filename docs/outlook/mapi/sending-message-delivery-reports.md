---
title: Senden von Nachrichtenübermittlungsberichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ef949db447aee54f0e007e1ddbbf104ea2451ef5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609439"
---
# <a name="sending-message-delivery-reports"></a>Senden von Nachrichtenübermittlungsberichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige zugrunde liegende Messagingsysteme unterstützen Übermittlungsberichte, andere nicht. Wie der Transportanbieter bestimmt, ob Nachrichtenübermittlungs- oder Unzustellbarkeitsberichte an Clientanwendungen gesendet werden können, ist ein für einzelne Transportanbieter spezifisches Implementierungsdetail. Wenn Übermittlungsberichte an Clientanwendungen gesendet werden können, verwenden Transportanbieter die [IMAPISupport::StatusRecips-Methode,](imapisupport-statusrecips.md) um die MAPI über eine erfolgreiche oder fehlerhafte Zustellung für einen oder mehrere Empfänger zu benachrichtigen. MAPI generiert dann Übermittlungs- oder Unzustellbarkeitsberichte, die diesen Empfängern entsprechen. Transportanbieter können auch eingehende Zustellungs- und Unzustellbarkeitsberichte, die im Messagingsystem systemintern sind, mit **statusrecips** in MAPI-Übermittlungs- und Nichtzustellbarkeitsberichte übersetzen.
  

