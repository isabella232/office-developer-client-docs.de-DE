---
title: Connect-Eigenschaft (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ebd9eb25e2e0e6b9b2233ff0d9faf8c3e369f0f9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925261"
---
# <a name="connect-property-rds"></a><span data-ttu-id="7c7d9-102">Connect-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="7c7d9-102">Connect property (RDS)</span></span>


<span data-ttu-id="7c7d9-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c7d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7c7d9-104">Gibt den Namen der Datenbank an, in der die Abfrage- und Aktualisierungsvorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7c7d9-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="7c7d9-105">Sie können die **Connect** -Eigenschaft zur Entwurfszeit in den OBJECT-Tags des [RDS.DataControl](datacontrol-object-rds.md)-Objekts bzw. zur Laufzeit im Skriptcode (z. B. VBScript) festlegen.</span><span class="sxs-lookup"><span data-stu-id="7c7d9-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="7c7d9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c7d9-106">Syntax</span></span>

<span data-ttu-id="7c7d9-107">Entwurfszeit: \<PARAM NAME = "Verbinden" Wert = "ConnectionString"\></span><span class="sxs-lookup"><span data-stu-id="7c7d9-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="7c7d9-108">Laufzeit: DataControl.Connect = "ConnectionString"</span><span class="sxs-lookup"><span data-stu-id="7c7d9-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="7c7d9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c7d9-109">Parameters</span></span>

- <span data-ttu-id="7c7d9-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="7c7d9-110">*ConnectionString*</span></span>

  - <span data-ttu-id="7c7d9-p101">Eine gültige Verbindungszeichenfolge. Allgemeinere Informationen zu Verbindungszeichenfolgen finden Sie im Abschnitt zur [ConnectionString](connectionstring-property-ado.md)-Eigenschaft oder in der Dokumentation Ihres Anbieters.</span><span class="sxs-lookup"><span data-stu-id="7c7d9-p101">A valid connection string. For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="7c7d9-p102">[!HINWEIS] Wenn Sie MS Remote als Anbieter für **RDS.DataControl** angeben, würde ein Szenario mit vier Ebenen erstellt. Szenarien mit mehr als drei Ebenen wurden nicht getestet und sollten nicht erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="7c7d9-p102">Specifying MS Remote as the provider for the **RDS.DataControl** would create a four-tier scenario. Scenarios greater than three tiers have not been tested and should not be needed.</span></span>

- <span data-ttu-id="7c7d9-115">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="7c7d9-115">*DataControl*</span></span>

  - <span data-ttu-id="7c7d9-116">Eine Objektvariable, die ein **RDS.DataControl**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="7c7d9-116">An object variable that represents an **RDS.DataControl** object.</span></span>

