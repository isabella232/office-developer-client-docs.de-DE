---
title: 'Kapitel 13: RDS-Auslastung und -Sicherheit'
TOCTitle: 'Chapter 13: RDS usage and security'
ms:assetid: 78add8bb-f01a-2efb-33f0-430deebefe8f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249495(v=office.15)
ms:contentKeyID: 48545756
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c0753a53a2001a6c5c96ae2ceb801ee6eb75a5e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716019"
---
# <a name="chapter-13-rds-usage-and-security"></a><span data-ttu-id="19c3b-102">Kapitel 13: RDS-Auslastung und -Sicherheit</span><span class="sxs-lookup"><span data-stu-id="19c3b-102">Chapter 13: RDS usage and security</span></span>

<span data-ttu-id="19c3b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="19c3b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="19c3b-p101">Mithilfe der Informationen in diesem Kapitel können Sie Ihren Server schnell einrichten und RDS (Remote Data Service) schnell verwenden. Dieses Kapitel umfasst spezielle Konfigurationsschritte, die Sie beim Implementieren von RDS durchführen müssen. Außerdem werden wichtige Beziehungen zwischen RDS und anderen Technologien erläutert und Lösungen für Probleme genannt, die während der Einrichtung einer RDS-Lösung auftreten können.</span><span class="sxs-lookup"><span data-stu-id="19c3b-p101">Use the information in this chapter to set up your server and use RDS quickly. This chapter includes specific configuration steps that you might need to take when implementing RDS, describes some of the key relationships between RDS and other technologies, and helps identify solutions to problems that you might encounter when setting up an RDS solution.</span></span>

<span data-ttu-id="19c3b-106">Dieser Abschnitt enthält Informationen zu folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="19c3b-106">This section contains information about:</span></span>

- [<span data-ttu-id="19c3b-107">Konfigurieren von DataFactory für den sicheren oder den uneingeschränkten Modus</span><span class="sxs-lookup"><span data-stu-id="19c3b-107">Configuring DataFactory for safe or unrestricted modes</span></span>](configuring-datafactory-for-safe-or-unrestricted-modes.md)
- [<span data-ttu-id="19c3b-108">Konfigurieren von RDS</span><span class="sxs-lookup"><span data-stu-id="19c3b-108">Configuring RDS</span></span>](configuring-rds.md)
- [<span data-ttu-id="19c3b-109">Konfigurieren von virtuellen Servern auf IIS</span><span class="sxs-lookup"><span data-stu-id="19c3b-109">Configuring virtual servers on IIS</span></span>](configuring-virtual-servers-on-iis.md)
- [<span data-ttu-id="19c3b-110">DataFactory-Anpassung (ADO)</span><span class="sxs-lookup"><span data-stu-id="19c3b-110">DataFactory customization (ADO)</span></span>](datafactory-customization.md)
- [<span data-ttu-id="19c3b-111">Aktivieren einer DLL zur Ausführung auf DCOM</span><span class="sxs-lookup"><span data-stu-id="19c3b-111">Enabling a DLL to run on DCOM</span></span>](enabling-a-dll-to-run-on-dcom.md)
- <span data-ttu-id="19c3b-112">[Gewähren einem Webservercomputer Gastberechtigungen; RDS Gast Berechtigungen \[ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span><span class="sxs-lookup"><span data-stu-id="19c3b-112">[Granting guest privileges to a web server computer; RDS guest privileges \[ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span></span>
- [<span data-ttu-id="19c3b-113">Kennzeichnen von Geschäftsobjekten als sicher für Skripting</span><span class="sxs-lookup"><span data-stu-id="19c3b-113">Marking business objects as safe for scripting</span></span>](marking-business-objects-as-safe-for-scripting.md)
- [<span data-ttu-id="19c3b-114">Registrieren von Geschäftsobjekten auf dem Client für die Verwendung mit DCOM</span><span class="sxs-lookup"><span data-stu-id="19c3b-114">Registering business objects on the client for use with DCOM</span></span>](registering-business-objects-on-the-client-for-use-with-dcom.md)
- [<span data-ttu-id="19c3b-115">Sichern von RDS-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="19c3b-115">Securing RDS applications</span></span>](securing-rds-applications.md)
- [<span data-ttu-id="19c3b-116">Festlegen des Formats für DCOM-Datenstrommarshalling</span><span class="sxs-lookup"><span data-stu-id="19c3b-116">Setting DCOM stream marshaling format</span></span>](setting-dcom-stream-marshaling-format.md)
- [<span data-ttu-id="19c3b-117">Angeben von Threads pro Prozessor auf IIS</span><span class="sxs-lookup"><span data-stu-id="19c3b-117">Specifying threads per processor on IIS</span></span>](specifying-threads-per-processor-on-iis.md)
- [<span data-ttu-id="19c3b-118">Troubleshooting RDS (ADO)</span><span class="sxs-lookup"><span data-stu-id="19c3b-118">Troubleshooting RDS (ADO)</span></span>](troubleshooting-rds.md)
- [<span data-ttu-id="19c3b-119">Verwenden verwandter Technologien mit RDS (ADO)</span><span class="sxs-lookup"><span data-stu-id="19c3b-119">Using related technologies with RDS (ADO)</span></span>](using-related-technologies-with-rds.md)














