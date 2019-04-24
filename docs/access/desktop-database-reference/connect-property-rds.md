---
title: Connect-Eigenschaft (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42e7dd643985cee9aef8887099eb90dcdb381f4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295982"
---
# <a name="connect-property-rds"></a><span data-ttu-id="3a1e3-102">Connect-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="3a1e3-102">Connect property (RDS)</span></span>

<span data-ttu-id="3a1e3-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a1e3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a1e3-104">Gibt den Namen der Datenbank an, in der die Abfrage- und Aktualisierungsvorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3a1e3-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="3a1e3-105">Sie können die **Connect**-Eigenschaft zur Entwurfszeit in den OBJECT-Tags des [RDS.DataControl](datacontrol-object-rds.md)-Objekts bzw. zur Laufzeit im Skriptcode (z. B. VBScript) festlegen.</span><span class="sxs-lookup"><span data-stu-id="3a1e3-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a1e3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a1e3-106">Syntax</span></span>

<span data-ttu-id="3a1e3-107">Entwurfszeit: \<Parameter Name = "Connect" Wert = "ConnectionString"\></span><span class="sxs-lookup"><span data-stu-id="3a1e3-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="3a1e3-108">Laufzeit: DataControl. Connect = "ConnectionString"</span><span class="sxs-lookup"><span data-stu-id="3a1e3-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="3a1e3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a1e3-109">Parameters</span></span>

|<span data-ttu-id="3a1e3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a1e3-110">Parameter</span></span>|<span data-ttu-id="3a1e3-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a1e3-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3a1e3-112">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="3a1e3-112">*ConnectionString*</span></span> |<span data-ttu-id="3a1e3-p101">Eine gültige Verbindungszeichenfolge. Allgemeinere Informationen zu Verbindungszeichenfolgen finden Sie im Abschnitt zur [ConnectionString](connectionstring-property-ado.md)-Eigenschaft oder in der Dokumentation Ihres Anbieters.</span><span class="sxs-lookup"><span data-stu-id="3a1e3-p101">A valid connection string. For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span><br/><br/><span data-ttu-id="3a1e3-115">**Hinweis**: Angeben von MS Remote als Anbieter für **RDS. DataControl** würde ein vierstufiges Szenario erstellen.</span><span class="sxs-lookup"><span data-stu-id="3a1e3-115">**NOTE**: Specifying MS Remote as the provider for the **RDS.DataControl** would create a four-tier scenario.</span></span> <span data-ttu-id="3a1e3-116">Szenarien mit mehr als drei Ebenen wurden nicht getestet und sollten nicht erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="3a1e3-116">Scenarios greater than three tiers have not been tested and should not be needed.</span></span>|
|<span data-ttu-id="3a1e3-117">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="3a1e3-117">*DataControl*</span></span> |<span data-ttu-id="3a1e3-118">Eine Objektvariable, die ein **RDS.DataControl**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="3a1e3-118">An object variable that represents an **RDS.DataControl** object.</span></span>|

