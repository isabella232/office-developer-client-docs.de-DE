---
title: Senden von Nachrichtenzustellungsberichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2a31e7d088d5c1f94b272cb4d307f3aff99f32ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433080"
---
# <a name="sending-message-delivery-reports"></a>Senden von Nachrichtenzustellungsberichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige zugrunde liegende Messagingsysteme unterstützen Übermittlungsberichte, andere nicht. Wie der Transportanbieter bestimmt, ob Nachrichtenzustellungs- oder Nicht-Zustellungsberichte an Clientanwendungen gesendet werden können, ist ein implementierungsspezifisches Detail für einzelne Transportanbieter. Wenn Übermittlungsberichte an Clientanwendungen gesendet werden können, verwenden Transportanbieter die [IMAPISupport::StatusRecips-Methode,](imapisupport-statusrecips.md) um MAPI über eine erfolgreiche oder nicht erfolgreiche Zustellung für einen oder mehrere Empfänger zu benachrichtigen. MAPI generiert dann Übermittlungs- oder Nichtzustellberichte, die diesen Empfängern entspricht. Transportanbieter können auch eingehende Zustellungs- und Nicht-Zustellungsberichte, die für das Messagingsystem nativ sind, mittels **StatusRecips** in MAPI-Übermittlungs- und Nicht-Zustellungsberichte übersetzen.
  

