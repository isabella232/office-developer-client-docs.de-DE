---
title: Verwalten von Nachrichten für POP3-Konten gedownloadet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b4218aa6-1591-49db-9782-f286135fc79a
description: Dieser Abschnitt beschreibt, wie der POP3-Anbieter von Outlook verwendet den eindeutigen ID auflisten (UIDL)-Verlauf auf ein POP3-Konto zur Identifikation von Nachrichten, die der Anbieter gedownloadet oder vom POP3-Server, um zu vermeiden, downloaden dieselbe Nachricht mehr als einmal gelöscht.
ms.openlocfilehash: 7661797193b0d64979cf58ca384a8359bfa59cfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791133"
---
# <a name="managing-message-downloads-for-pop3-accounts"></a>Verwalten von Nachrichten für POP3-Konten gedownloadet

Dieser Abschnitt beschreibt, wie der POP3-Anbieter von Outlook verwendet den eindeutigen ID auflisten (UIDL)-Verlauf auf ein POP3-Konto zur Identifikation von Nachrichten, die der Anbieter gedownloadet oder vom POP3-Server, um zu vermeiden, downloaden dieselbe Nachricht mehr als einmal gelöscht.
  
## <a name="introduction-to-pop"></a>Einführung in POP

Das Post Office Protocol (POP) gibt ein Protokoll auf Anwendungsebene für ein e-Mail-Client wie z. B. Outlook e-Mail-Nachrichten von einem e-Mail-Server herunterladen. Es ermöglicht einem Benutzer einer Kopie einer e-Mail-Nachricht auf einem lokalen Gerät (z. B. einem Smartphone oder Computer) und lassen eine Kopie auf dem Server oder löschen Sie ihn. Das Protokoll unterstützt nur ein e-Mail-Client mit dem Postfach gleichzeitig verbunden sein. Es gibt nur abrufen, jedoch nicht vom Mail-Server e-Mail-Nachrichten senden. Wenn Sie POP verwenden, ein e-Mail-Client in der Regel zu prüfen, ob neue e-Mail-Nachrichten, verbindet mit dem Mail-Server für nur den Betrag der Zeit neue Nachrichten herunterzuladen, und nicht mit dem Server, um neue e-Mail-Benachrichtigungen erhalten bleiben. POP unterstützt nur e-Mail-Nachrichten jedoch nicht anderen Elementtypen wie Kontakte und Termine, es sei denn, sie in eine e-Mail-Nachricht gekapselt sind. POP3 ist Version 3 des Protokolls.
  
Nachrichten für ein POP-Konto werden durch eindeutige Bezeichner (UIDs) identifiziert. Ein e-Mail-Client, der e-Mail-Nachrichten auf dem Server lässt verwendet den UIDL-Befehl UIDL-Karte abrufen, die jede Nachricht zuordnet, die auf das Postfach, um die UID geliefert wurde. Der Client erhält den UIDL-Verlauf auch für Nachrichten, die gedownloadet oder für den Posteingang auf dem Client gelöscht wurden. Basierend auf den UIDL-Verlauf, kann der Client bestimmen, welche Nachrichten sind neu und heruntergeladen werden sollen.

- [Suchen die Nachricht Downloadverlauf für ein POP3-Konto](locating-the-message-download-history-for-a-pop3-account.md): in diesem Thema wird beschrieben, wie die [PidTagAttachDataBinary](http://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) -Eigenschaft, um den Verlauf UIDL für Nachrichten im Posteingang des POP3-Konto-Client Abrufen von e-Mail-Client greift auf. 
    
- [Analysieren der Nachricht Downloadverlauf für ein POP3-Konto](parsing-the-message-download-history-for-a-pop3-account.md): in diesem Thema wird beschrieben, wie das BLOB POP3 analysiert, die den Verlauf UIDL für Nachrichten im Posteingang des POP3-Konto-Client zur Kennzeichnung der Nachrichten, die heruntergeladen oder auf, die gelöscht wurden darstellt Konto.
    
## <a name="see-also"></a>Siehe auch

- [Outlook-Account-management](outlook-account-management.md)    
- [Suchen den Nachrichten-Downloadverlauf für ein POP3-Konto](locating-the-message-download-history-for-a-pop3-account.md) 
- [Analysieren den Nachrichten-Downloadverlauf für ein POP3-Konto](parsing-the-message-download-history-for-a-pop3-account.md)   
- [PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)    
- [Eigenschaften (Account Management API)](properties-account-management-api.md)
    

