---
title: Exchange-Benutzer
TOCTitle: Exchange users
ms:assetid: 01802032-fd60-400b-ad83-1f4eefe596bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184585(v=office.15)
ms:contentKeyID: 55119835
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 667f8a07477c527d251c4e50f35baa2da2e417ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357834"
---
# <a name="exchange-users"></a>Exchange-Benutzer

In diesem Abschnitt werden Beispielaufgaben bereitgestellt, die sich auf Microsoft Exchange-Postfachbenutzer beziehen. Exchange-Benutzer sind mit einem Exchange-Server verbunden und werden von [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) -Objekten dargestellt, die vom [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) -Objekt abgeleitet sind.

## <a name="in-this-section"></a>Inhalt dieses Abschnitts

|Thema|Beschreibung|
|:----|:----------|
|[Abrufen von Informationen über den aktuellen Benutzer](how-to-get-information-about-the-current-user.md)  |Ruft die Informationen des aktuellen Benutzers ab, z. B. Name, berufliche Position und Telefonnummer.|
|[Abrufen von Informationen über alle Verteilerlisten, in denen der aktuelle Benutzer Mitglied ist](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)  |Verwendet die [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\))-Methode zum Abrufen von Informationen über alle Verteilerlisten, in denen der aktuelle Benutzer Mitglied ist.|
|[Erstellen einer Verteilerliste](how-to-create-a-distribution-list.md)  |Erstellt eine Verteilerliste und zeigt diesem dem Benutzer an.|
[Abrufen der Mitglieder einer Exchange-Verteilerliste](how-to-get-members-of-an-exchange-distribution-list.md)  |Fordert den Benutzer auf, eine Exchange-Verteilerliste im Dialogfeld **Namen auswählen** auszuwählen, und gliedert diese Verteilerliste auf, um die Mitglieder anzuzeigen.|
[Abrufen von Informationen zum Vorgesetzten des aktuellen Benutzers](how-to-get-information-about-the-current-user-s-manager.md)  |Ruft Informationen (z. B. Name, berufliche Position und Telefonnummern) zum Vorgesetzten des aktuellen Benutzers ab.|
[Abrufen von Verfügbarkeitsinformationen für den Vorgesetzten eines Exchange-Benutzers](how-to-get-availability-information-for-an-exchange-user-s-manager.md) |  Zeigt das nächste freie 60-minütige Zeitfenster für den Vorgesetzten eines Benutzers im Kalender an.|
|[Überprüfen der Antwort eines Vorgesetzten auf eine Besprechungsanfrage](how-to-check-a-manager-s-response-to-a-meeting-request.md) | Verwendet die [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\))- und die [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\))-Methode, um den Status der Antwort des Vorgesetzten des aktuellen Benutzers auf eine Besprechungsanfrage zu überprüfen.|
|[Abrufen von Informationen zu direkten Mitarbeitern des Vorgesetzten des aktuellen Benutzers](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md) | Ruft die direkten Mitarbeiter des Vorgesetzten des aktuellen Benutzers ab, sofern vorhanden, und zeigt dann Informationen zu den einzelnen direkten Mitarbeiter des Vorgesetzten an.|

## <a name="see-also"></a>Siehe auch

- [Konten](accounts.md)
- [Adressbuch](address-book.md)
- [Speicher](stores.md)
- [Gewusst wie... (Outlook 2013 PIA-Referenz)](how-do-i-outlook-2013-pia-reference.md)

