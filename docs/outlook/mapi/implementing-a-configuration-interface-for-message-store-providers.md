---
title: Implementieren einer Konfigurationsschnittstelle für Nachrichtenspeicher-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f7151841eef180a78a13ad161d197af783decfb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792516"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>Implementieren einer Konfigurationsschnittstelle für Nachrichtenspeicher-Anbieter

  
  
**Betrifft**: Outlook 
  
Nachricht-Anbieter werden benötigt, um eine Schnittstelle implementieren, die dem Benutzer ermöglicht, konfigurieren Sie den Nachricht Speicheranbieter auf dem Computer des Benutzers ausgeführt. Der Nachricht Speicheranbieter wird normalerweise konfiguriert, wenn der Nachricht Speicheranbieter Profil eines Benutzers hinzugefügt wird. Verarbeitet die Nachricht Speicheranbieter Konfiguration-Schnittstelle im allgemeinen Aufgaben wie das Festlegen von Benutzernamen und Kennwörter für geschützte Nachrichtenspeicher Pfade zu erforderlichen Dateien auswählen, und erstellen den zugrunde liegende Speichermechanismus wird verwendet, falls erforderlich.
  
Der Zugriff auf die Konfigurationsschnittstelle, die Sie implementieren erfolgt über zusätzliche Einstiegspunkte in Ihren Dienstanbieter Nachricht DLL-Datei. Weitere Informationen finden Sie unter [Konfigurieren eines Diensts Nachricht](configuring-a-message-service.md). Die Nachricht Speicheranbieter Konfigurationsschnittstelle ist die einzige Benutzeroberfläche, die eine Nachricht Speicheranbieter implementieren müssen.
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

