---
title: Minimieren der Speicherverwendung der Protokolldatei
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c8d582d55596b7d19220580bc2e670e92bfeb0ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602206"
---
# <a name="minimizing-log-file-space-usage"></a>Minimieren der Speicherverwendung der Protokolldatei

**Gilt für**: Access 2013, Office 2013

Eine Protokolldatei kann sich schnell füllen (und somit den Server verlangsamen), wenn in einer SQL Server-Datenbank Aktivitäten in großem Umfang ausgeführt werden. Sie können für die Protokolldatei **Protokoll bei Prüfpunkt abschneiden** festlegen, um die Nutzungsdauer der Protokolldatei für eine Datenbank erheblich zu verlängern.

**So aktivieren Sie "Protokoll bei Prüfpunkt abschneiden" in Microsoft SQL Server 6.5**

1.  Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.

2.  Doppelklicken Sie auf den Namen der Datenbank, für die Sie dieses Feature aktivieren möchten.

3.  Wählen Sie auf der Registerkarte **Datenbank** die Option **Abschneiden** aus.

4.  Wählen Sie auf der Registerkarte **Optionen** die Option **Protokoll bei Prüfpunkt abschneiden** aus, und klicken Sie dann auf **OK**.

**So aktivieren Sie "Protokoll bei Prüfpunkt abschneiden" in Microsoft SQL Server 7.0**

1.  Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Databases tree.

2.  Klicken Sie mit der rechten Maustaste auf den Namen der Datenbank, für die Sie dieses Feature aktivieren möchten, und wählen Sie dann **Eigenschaften** aus.

3.  Wählen Sie auf der Registerkarte **Optionen** die Option **Protokoll bei Prüfpunkt abschneiden** aus, und klicken Sie dann auf **OK**.

Weitere Informationen zum Feature **Protokoll bei Prüfpunkt abschneiden** finden Sie in der Microsoft SQL Server-Dokumentation.

