---
title: Connect-Eigenschaft (RDS)
TOCTitle: Connect Property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d9b901f925ccc009a12ef527f7bc857515042c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872403"
---
# <a name="connect-property-rds"></a><span data-ttu-id="8f56c-102">Connect-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="8f56c-102">Connect Property (RDS)</span></span>


<span data-ttu-id="8f56c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f56c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8f56c-104">Gibt den Namen der Datenbank an, in der die Abfrage- und Aktualisierungsvorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8f56c-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="8f56c-105">Sie können die **Connect** -Eigenschaft zur Entwurfszeit in den OBJECT-Tags des [RDS.DataControl](datacontrol-object-rds.md)-Objekts bzw. zur Laufzeit im Skriptcode (z. B. VBScript) festlegen.</span><span class="sxs-lookup"><span data-stu-id="8f56c-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f56c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f56c-106">Syntax</span></span>

<span data-ttu-id="8f56c-107">Entwurfszeit: \<PARAM NAME = "Verbinden" Wert = "ConnectionString"\></span><span class="sxs-lookup"><span data-stu-id="8f56c-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="8f56c-108">Laufzeit: DataControl.Connect = "ConnectionString"</span><span class="sxs-lookup"><span data-stu-id="8f56c-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="8f56c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f56c-109">Parameters</span></span>

- <span data-ttu-id="8f56c-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="8f56c-110">*ConnectionString*</span></span>

  - <span data-ttu-id="8f56c-p101">Eine gültige Verbindungszeichenfolge. Allgemeinere Informationen zu Verbindungszeichenfolgen finden Sie im Abschnitt zur [ConnectionString](connectionstring-property-ado.md)-Eigenschaft oder in der Dokumentation Ihres Anbieters.</span><span class="sxs-lookup"><span data-stu-id="8f56c-p101">A valid connection string. For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8f56c-p102">[!HINWEIS] Wenn Sie MS Remote als Anbieter für **RDS.DataControl** angeben, würde ein Szenario mit vier Ebenen erstellt. Szenarien mit mehr als drei Ebenen wurden nicht getestet und sollten nicht erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="8f56c-p102">Specifying MS Remote as the provider for the **RDS.DataControl** would create a four-tier scenario. Scenarios greater than three tiers have not been tested and should not be needed.</span></span>

- <span data-ttu-id="8f56c-115">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="8f56c-115">*DataControl*</span></span>

  - <span data-ttu-id="8f56c-116">Eine Objektvariable, die ein **RDS.DataControl**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8f56c-116">An object variable that represents an **RDS.DataControl** object.</span></span>

