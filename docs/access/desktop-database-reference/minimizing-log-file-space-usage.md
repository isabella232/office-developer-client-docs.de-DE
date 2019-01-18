---
title: Minimieren der Speicherverwendung der Protokolldatei
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: da4bf7c9c30d3b9b37e2835ddeeeab2b2ed8a2c6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715277"
---
# <a name="minimizing-log-file-space-usage"></a>Minimieren der Speicherverwendung der Protokolldatei

**Betrifft**: Access 2013, Office 2013

Eine Protokolldatei kann sich schnell füllen (und somit den Server verlangsamen), wenn in einer SQL Server-Datenbank Aktivitäten in großem Umfang ausgeführt werden. Sie können für die Protokolldatei **Protokoll bei Prüfpunkt abschneiden** festlegen, um die Nutzungsdauer der Protokolldatei für eine Datenbank erheblich zu verlängern.

**So aktivieren Sie "Protokoll bei Prüfpunkt abschneiden" in Microsoft SQL Server 6.5**

1.  Starten Sie Microsoft SQL Server Enterprise Manager, öffnen Sie die Struktur für den Server, und öffnen Sie dann die Struktur Datenbankmedien.

2.  Doppelklicken Sie auf den Namen der Datenbank, für die Sie dieses Feature aktivieren möchten.

3.  Wählen Sie auf der Registerkarte **Datenbank** die Option **Abschneiden** aus.

4.  Wählen Sie auf der Registerkarte **Optionen** die Option **Protokoll bei Prüfpunkt abschneiden** aus, und klicken Sie dann auf **OK**.

**So aktivieren Sie "Protokoll bei Prüfpunkt abschneiden" in Microsoft SQL Server 7.0**

1.  Starten Sie Microsoft SQL Server Enterprise Manager, öffnen Sie die Struktur für den Server, und öffnen Sie dann die Struktur Datenbanken.

2.  Klicken Sie mit der rechten Maustaste auf den Namen der Datenbank, für die Sie dieses Feature aktivieren möchten, und wählen Sie dann **Eigenschaften** aus.

3.  Wählen Sie auf der Registerkarte **Optionen** die Option **Protokoll bei Prüfpunkt abschneiden** aus, und klicken Sie dann auf **OK**.

Weitere Informationen zum Feature **Protokoll bei Prüfpunkt abschneiden** finden Sie in der Microsoft SQL Server-Dokumentation.

