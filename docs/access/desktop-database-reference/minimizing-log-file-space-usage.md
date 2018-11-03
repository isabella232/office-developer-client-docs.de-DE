---
title: Minimieren der speicherplatznutzung von Protokolldateien
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2c462641616c126c7732433fc8b7d23bb137b06a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944767"
---
# <a name="minimizing-log-file-space-usage"></a><span data-ttu-id="969d0-102">Minimieren der speicherplatznutzung von Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="969d0-102">Minimizing log file space usage</span></span>

<span data-ttu-id="969d0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="969d0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="969d0-p101">Eine Protokolldatei kann sich schnell füllen (und somit den Server verlangsamen), wenn in einer SQL Server-Datenbank Aktivitäten in großem Umfang ausgeführt werden. Sie können für die Protokolldatei **Protokoll bei Prüfpunkt abschneiden** festlegen, um die Nutzungsdauer der Protokolldatei für eine Datenbank erheblich zu verlängern.</span><span class="sxs-lookup"><span data-stu-id="969d0-p101">A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database. You can set the log file to **Truncate on Checkpoint** to significantly extend the life of the log file for a database.</span></span>

<span data-ttu-id="969d0-106">**So aktivieren Sie "Protokoll bei Prüfpunkt abschneiden" in Microsoft SQL Server 6.5**</span><span class="sxs-lookup"><span data-stu-id="969d0-106">**To enable Truncate on Checkpoint in Microsoft SQL Server 6.5**</span></span>

1.  <span data-ttu-id="969d0-107">Starten Sie Microsoft SQL Server Enterprise Manager, öffnen Sie die Struktur für den Server, und öffnen Sie dann die Struktur Datenbankmedien.</span><span class="sxs-lookup"><span data-stu-id="969d0-107">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="969d0-108">Doppelklicken Sie auf den Namen der Datenbank, für die Sie dieses Feature aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="969d0-108">Double-click the name of the database on which this feature will be enabled.</span></span>

3.  <span data-ttu-id="969d0-109">Wählen Sie auf der Registerkarte **Datenbank** die Option **Abschneiden** aus.</span><span class="sxs-lookup"><span data-stu-id="969d0-109">From the **Database** tab, select **Truncate**.</span></span>

4.  <span data-ttu-id="969d0-110">Wählen Sie auf der Registerkarte **Optionen** die Option **Protokoll bei Prüfpunkt abschneiden** aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="969d0-110">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="969d0-111">**So aktivieren Sie "Protokoll bei Prüfpunkt abschneiden" in Microsoft SQL Server 7.0**</span><span class="sxs-lookup"><span data-stu-id="969d0-111">**To enable Truncate on Checkpoint in Microsoft SQL Server 7.0**</span></span>

1.  <span data-ttu-id="969d0-112">Starten Sie Microsoft SQL Server Enterprise Manager, öffnen Sie die Struktur für den Server, und öffnen Sie dann die Struktur Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="969d0-112">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Databases tree.</span></span>

2.  <span data-ttu-id="969d0-113">Klicken Sie mit der rechten Maustaste auf den Namen der Datenbank, für die Sie dieses Feature aktivieren möchten, und wählen Sie dann **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="969d0-113">Right-click the name of the database on which this feature will be enabled and choose **Properties**.</span></span>

3.  <span data-ttu-id="969d0-114">Wählen Sie auf der Registerkarte **Optionen** die Option **Protokoll bei Prüfpunkt abschneiden** aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="969d0-114">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="969d0-115">Weitere Informationen zum Feature **Protokoll bei Prüfpunkt abschneiden** finden Sie in der Microsoft SQL Server-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="969d0-115">For more information about the **Truncate on Checkpoint** feature, see the Microsoft SQL Server documentation.</span></span>

