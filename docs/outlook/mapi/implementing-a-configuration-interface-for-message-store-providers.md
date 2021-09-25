---
title: Implementieren einer Konfigurationsschnittstelle für Nachrichtenanbieter Store
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 56ef4e25ad432acc42959aa1b6034ad0c02add31
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575652"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>Implementieren einer Konfigurationsschnittstelle für Nachrichtenanbieter Store

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicheranbieter müssen eine Schnittstelle implementieren, die es dem Benutzer ermöglicht, den Nachrichtenspeicheranbieter für die Ausführung auf dem Computer dieses Benutzers zu konfigurieren. In der Regel wird der Nachrichtenspeicheranbieter konfiguriert, wenn der Nachrichtenspeicheranbieter dem Profil eines Benutzers hinzugefügt wird. Die Konfigurationsschnittstelle des Nachrichtenspeicheranbieters übernimmt in der Regel Aufgaben wie das Festlegen von Benutzernamen und Kennwörtern für geschützte Nachrichtenspeicher, das Auswählen von Pfaden zu erforderlichen Dateien und das Erstellen des zugrunde liegenden Speichermechanismus, der bei Bedarf verwendet wird.
  
Der Zugriff auf die von Ihnen implementierte Konfigurationsschnittstelle erfolgt über zusätzliche Einstiegspunkte in der DLL Ihres Nachrichtendienstanbieters. Weitere Informationen finden Sie unter [Konfigurieren eines Nachrichtendiensts.](configuring-a-message-service.md) Die Konfigurationsschnittstelle des Nachrichtenspeicheranbieters ist die einzige Benutzeroberfläche, die ein Nachrichtenspeicheranbieter implementieren muss.
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

