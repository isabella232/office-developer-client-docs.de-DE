---
title: Dynamische Recordset-Eigenschaften in XML
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf2a15937f6bcfd9ededcfad0cf15c29faf6e577
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307658"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="c28fd-102">Dynamische Recordset-Eigenschaften in XML</span><span class="sxs-lookup"><span data-stu-id="c28fd-102">Recordset dynamic properties in XML</span></span>

<span data-ttu-id="c28fd-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c28fd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c28fd-104">Die folgenden anbieterspezifischen Eigenschaften des **Recordset** -Objekts (im Client Cursor Engine) werden derzeit im XML-Format gespeichert:</span><span class="sxs-lookup"><span data-stu-id="c28fd-104">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

- <span data-ttu-id="c28fd-105">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="c28fd-105">**AutoRecalc**</span></span>
- <span data-ttu-id="c28fd-106">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="c28fd-106">**BatchSize**</span></span>
- <span data-ttu-id="c28fd-107">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="c28fd-107">**CommandTimeout**</span></span>
- <span data-ttu-id="c28fd-108">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="c28fd-108">**IRowsetChange**</span></span>
- <span data-ttu-id="c28fd-109">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="c28fd-109">**IRowsetUpdate**</span></span>
- <span data-ttu-id="c28fd-110">**Reshape Name**</span><span class="sxs-lookup"><span data-stu-id="c28fd-110">**Reshape Name**</span></span>
- <span data-ttu-id="c28fd-111">**Resync Command**</span><span class="sxs-lookup"><span data-stu-id="c28fd-111">**Resync Command**</span></span>
- <span data-ttu-id="c28fd-112">**Unique Catalog**</span><span class="sxs-lookup"><span data-stu-id="c28fd-112">**Unique Catalog**</span></span>
- <span data-ttu-id="c28fd-113">**Unique Schema**</span><span class="sxs-lookup"><span data-stu-id="c28fd-113">**Unique Schema**</span></span>
- <span data-ttu-id="c28fd-114">**Unique Table**</span><span class="sxs-lookup"><span data-stu-id="c28fd-114">**Unique Table**</span></span>
- <span data-ttu-id="c28fd-115">**Update Resync**</span><span class="sxs-lookup"><span data-stu-id="c28fd-115">**Update Resync**</span></span>
- <span data-ttu-id="c28fd-116">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="c28fd-116">**UpdateCriteria**</span></span>


<span data-ttu-id="c28fd-p101">Diese Eigenschaften werden im Schemaabschnitt als Attribute der Elementdefinition für das **Recordset** -Objekt gespeichert. Diese Attribute werden im Rowsetschemanamespace definiert und müssen das Präfix "rs:" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c28fd-p101">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted. These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

## <a name="see-also"></a><span data-ttu-id="c28fd-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c28fd-119">See also</span></span>

- [<span data-ttu-id="c28fd-120">Dynamische ADO-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c28fd-120">ADO dynamic properties</span></span>](ado-dynamic-properties.md)
