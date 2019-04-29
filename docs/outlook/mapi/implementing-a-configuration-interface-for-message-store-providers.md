---
title: Implementieren einer Konfigurationsschnittstelle für Nachrichtenspeicher Anbieter
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
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>Implementieren einer Konfigurationsschnittstelle für Nachrichtenspeicher Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicher Anbieter müssen eine Schnittstelle implementieren, die es dem Benutzer ermöglicht, den Nachrichtenspeicher Anbieter so zu konfigurieren, dass er auf dem Computer des Benutzers ausgeführt wird. In der Regel wird der Nachrichtenspeicher Anbieter konfiguriert, wenn der Nachrichtenspeicher Anbieter dem Benutzerprofil hinzugefügt wird. Die Konfigurationsschnittstelle des Nachrichtenspeicher Anbieters verarbeitet in der Regelaufgaben wie das Festlegen von Benutzernamen und Kennwörtern für geschützte Nachrichtenspeicher, das Auswählen von Pfaden zu den erforderlichen Dateien und das Erstellen des zugrunde liegenden Speichermechanismus, der bei Bedarf verwendet wird.
  
Der Zugriff auf die Konfigurationsschnittstelle, die Sie implementieren, erfolgt über zusätzliche Einstiegspunkte in der DLL des Nachrichten Dienstanbieters. Weitere Informationen finden Sie unter [Konfigurieren eines Nachrichtendiensts](configuring-a-message-service.md). Die Konfigurationsschnittstelle des Nachrichtenspeicher Anbieters ist die einzige Benutzeroberfläche, die ein Nachrichtenspeicher Anbieter implementieren muss.
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

