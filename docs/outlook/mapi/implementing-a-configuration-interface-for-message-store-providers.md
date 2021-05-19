---
title: Implementieren einer Konfigurationsschnittstelle für Store-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415887"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>Implementieren einer Konfigurationsschnittstelle für Store-Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicheranbieter müssen eine Schnittstelle implementieren, die es dem Benutzer ermöglicht, den Nachrichtenspeicheranbieter für die Ausführung auf dem Computer dieses Benutzers zu konfigurieren. In der Regel wird der Nachrichtenspeicheranbieter konfiguriert, wenn der Nachrichtenspeicheranbieter dem Profil eines Benutzers hinzugefügt wird. Die Konfigurationsschnittstelle des Nachrichtenspeicheranbieters übernimmt in der Regel Aufgaben wie das Festlegen von Benutzernamen und Kennwörtern für geschützte Nachrichtenspeicher, das Auswählen von Pfaden zu den erforderlichen Dateien und das Erstellen des zugrunde liegenden Speichermechanismus, den er bei Bedarf verwendet.
  
Der Zugriff auf die von Ihnen implementierte Konfigurationsschnittstelle wird über zusätzliche Einstiegspunkte in der DLL des Nachrichtendienstanbieters ermöglicht. Weitere Informationen finden Sie unter [Configuring a Message Service](configuring-a-message-service.md). Die Konfigurationsschnittstelle des Nachrichtenspeicheranbieters ist die einzige Benutzeroberfläche, die ein Nachrichtenspeicheranbieter implementieren muss.
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

