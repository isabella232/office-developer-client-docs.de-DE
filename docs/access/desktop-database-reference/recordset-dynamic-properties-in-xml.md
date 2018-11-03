---
title: Dynamische Recordset-Eigenschaften in XML
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36069ec0e8e9020bc70ef1ea72ce25f4461c6487
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946958"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="37f8a-102">Dynamische Recordset-Eigenschaften in XML</span><span class="sxs-lookup"><span data-stu-id="37f8a-102">Recordset dynamic properties in XML</span></span>

<span data-ttu-id="37f8a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="37f8a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37f8a-104">Die folgenden anbieterspezifischen Eigenschaften des **Recordset** -Objekts (im Client Cursor Engine) werden derzeit im XML-Format gespeichert:</span><span class="sxs-lookup"><span data-stu-id="37f8a-104">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

- <span data-ttu-id="37f8a-105">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="37f8a-105">**AutoRecalc**</span></span>
- <span data-ttu-id="37f8a-106">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="37f8a-106">**BatchSize**</span></span>
- <span data-ttu-id="37f8a-107">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="37f8a-107">**CommandTimeout**</span></span>
- <span data-ttu-id="37f8a-108">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="37f8a-108">**IRowsetChange**</span></span>
- <span data-ttu-id="37f8a-109">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="37f8a-109">**IRowsetUpdate**</span></span>
- <span data-ttu-id="37f8a-110">**Reshape Name**</span><span class="sxs-lookup"><span data-stu-id="37f8a-110">**Reshape Name**</span></span>
- <span data-ttu-id="37f8a-111">**Resync Command**</span><span class="sxs-lookup"><span data-stu-id="37f8a-111">**Resync Command**</span></span>
- <span data-ttu-id="37f8a-112">**Unique Catalog**</span><span class="sxs-lookup"><span data-stu-id="37f8a-112">**Unique Catalog**</span></span>
- <span data-ttu-id="37f8a-113">**Unique Schema**</span><span class="sxs-lookup"><span data-stu-id="37f8a-113">**Unique Schema**</span></span>
- <span data-ttu-id="37f8a-114">**Unique Table**</span><span class="sxs-lookup"><span data-stu-id="37f8a-114">**Unique Table**</span></span>
- <span data-ttu-id="37f8a-115">**Update Resync**</span><span class="sxs-lookup"><span data-stu-id="37f8a-115">**Update Resync**</span></span>
- <span data-ttu-id="37f8a-116">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="37f8a-116">**UpdateCriteria**</span></span>


<span data-ttu-id="37f8a-p101">Diese Eigenschaften werden im Schemaabschnitt als Attribute der Elementdefinition für das **Recordset** -Objekt gespeichert. Diese Attribute werden im Rowsetschemanamespace definiert und müssen das Präfix "rs:" enthalten.</span><span class="sxs-lookup"><span data-stu-id="37f8a-p101">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted. These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

## <a name="see-also"></a><span data-ttu-id="37f8a-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37f8a-119">See also</span></span>

- [<span data-ttu-id="37f8a-120">Dynamische ADO-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37f8a-120">ADO dynamic properties</span></span>](ado-dynamic-properties.md)