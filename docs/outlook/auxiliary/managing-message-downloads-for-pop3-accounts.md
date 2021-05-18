---
title: Verwalten von Nachrichten für POP3-Konten gedownloadet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b4218aa6-1591-49db-9782-f286135fc79a
description: Dieser Abschnitt beschreibt, wie der POP3-Anbieter von Outlook verwendet den eindeutigen ID auflisten (UIDL)-Verlauf auf ein POP3-Konto zur Identifikation von Nachrichten, die der Anbieter gedownloadet oder vom POP3-Server, um zu vermeiden, downloaden dieselbe Nachricht mehr als einmal gelöscht.
ms.openlocfilehash: 35c50d83c317ebefa52fd9bfcb348c8411a06f25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322246"
---
# <a name="managing-message-downloads-for-pop3-accounts"></a>Verwalten von Nachrichten für POP3-Konten gedownloadet

Dieser Abschnitt beschreibt, wie der POP3-Anbieter von Outlook verwendet den eindeutigen ID auflisten (UIDL)-Verlauf auf ein POP3-Konto zur Identifikation von Nachrichten, die der Anbieter gedownloadet oder vom POP3-Server, um zu vermeiden, downloaden dieselbe Nachricht mehr als einmal gelöscht.
  
## <a name="introduction-to-pop"></a>Einführung in POP

Das Post Office Protocol (POP) gibt ein Protokoll auf Anwendungsebene für ein e-Mail-Client wie z. B. Outlook e-Mail-Nachrichten von einem e-Mail-Server herunterladen. Es ermöglicht einem Benutzer einer Kopie einer e-Mail-Nachricht auf einem lokalen Gerät (z. B. einem Smartphone oder Computer) und lassen eine Kopie auf dem Server oder löschen Sie ihn. Das Protokoll unterstützt nur ein e-Mail-Client mit dem Postfach gleichzeitig verbunden sein. Es gibt nur abrufen, jedoch nicht vom Mail-Server e-Mail-Nachrichten senden. Wenn Sie POP verwenden, ein e-Mail-Client in der Regel zu prüfen, ob neue e-Mail-Nachrichten, verbindet mit dem Mail-Server für nur den Betrag der Zeit neue Nachrichten herunterzuladen, und nicht mit dem Server, um neue e-Mail-Benachrichtigungen erhalten bleiben. POP unterstützt nur e-Mail-Nachrichten jedoch nicht anderen Elementtypen wie Kontakte und Termine, es sei denn, sie in eine e-Mail-Nachricht gekapselt sind. POP3 ist Version 3 des Protokolls.
  
Nachrichten für ein POP-Konto werden durch eindeutige Bezeichner (UIDs) identifiziert. Ein e-Mail-Client, der e-Mail-Nachrichten auf dem Server lässt verwendet den UIDL-Befehl UIDL-Karte abrufen, die jede Nachricht zuordnet, die auf das Postfach, um die UID geliefert wurde. Der Client erhält den UIDL-Verlauf auch für Nachrichten, die gedownloadet oder für den Posteingang auf dem Client gelöscht wurden. Basierend auf den UIDL-Verlauf, kann der Client bestimmen, welche Nachrichten sind neu und heruntergeladen werden sollen.

- Suchen des Nachrichtendownloadverlaufs für ein [POP3-Konto:](locating-the-message-download-history-for-a-pop3-account.md)In diesem Thema wird beschrieben, wie ein E-Mail-Client auf die [PidTagAttachDataBinary-Eigenschaft](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) zusteuert, um den #A0 für Nachrichten im Client posteingang eines POP3-Kontos zu erhalten. 
    
- [Analysieren](parsing-the-message-download-history-for-a-pop3-account.md)des Nachrichtendownloadverlaufs für ein POP3-Konto: In diesem Thema wird beschrieben, wie sie den POP3-BLOB analysieren, der den UIDL-Verlauf für Nachrichten im Client posteingang eines POP3-Kontos darstellt, um die Nachrichten zu identifizieren, die für dieses Konto heruntergeladen oder gelöscht wurden.
    
## <a name="see-also"></a>Siehe auch

- [Outlook-Account-management](outlook-account-management.md)    
- [Suchen den Nachrichten-Downloadverlauf für ein POP3-Konto](locating-the-message-download-history-for-a-pop3-account.md) 
- [Analysieren den Nachrichten-Downloadverlauf für ein POP3-Konto](parsing-the-message-download-history-for-a-pop3-account.md)   
- [PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)    
- [Eigenschaften (Account Management API)](properties-account-management-api.md)
    

