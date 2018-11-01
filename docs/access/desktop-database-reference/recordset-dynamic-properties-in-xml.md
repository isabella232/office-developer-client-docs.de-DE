---
title: Dynamische Eigenschaften des Recordset-Objekts in XML
TOCTitle: Recordset Dynamic Properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 48714b9178e99cfd4ccf7738f3ad4a342572fdfa
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884261"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="b9cc2-102">Dynamische Eigenschaften des Recordset-Objekts in XML</span><span class="sxs-lookup"><span data-stu-id="b9cc2-102">Recordset Dynamic Properties in XML</span></span>


<span data-ttu-id="b9cc2-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9cc2-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="b9cc2-104">Dynamische Eigenschaften des Recordset-Objekts in XML</span><span class="sxs-lookup"><span data-stu-id="b9cc2-104">Recordset Dynamic Properties in XML</span></span>

<span data-ttu-id="b9cc2-105">Die folgenden anbieterspezifischen Eigenschaften des **Recordset** -Objekts (im Client Cursor Engine) werden derzeit im XML-Format gespeichert:</span><span class="sxs-lookup"><span data-stu-id="b9cc2-105">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

  - <span data-ttu-id="b9cc2-106">**Update Resync**</span><span class="sxs-lookup"><span data-stu-id="b9cc2-106">**Update Resync**</span></span>

  - <span data-ttu-id="b9cc2-107">**Unique Table**</span><span class="sxs-lookup"><span data-stu-id="b9cc2-107">**Unique Table**</span></span>

  - <span data-ttu-id="b9cc2-108">**Unique Schema**</span><span class="sxs-lookup"><span data-stu-id="b9cc2-108">**Unique Schema**</span></span>

  - <span data-ttu-id="b9cc2-109">**Unique Catalog**</span><span class="sxs-lookup"><span data-stu-id="b9cc2-109">**Unique Catalog**</span></span>

  - <span data-ttu-id="b9cc2-110">**Resync Command**</span><span class="sxs-lookup"><span data-stu-id="b9cc2-110">**Resync Command**</span></span>

  - <span data-ttu-id="b9cc2-111">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="b9cc2-111">**IRowsetChange**</span></span>

  - <span data-ttu-id="b9cc2-112">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="b9cc2-112">**IRowsetUpdate**</span></span>

  - <span data-ttu-id="b9cc2-113">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="b9cc2-113">**CommandTimeout**</span></span>

  - <span data-ttu-id="b9cc2-114">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="b9cc2-114">**BatchSize**</span></span>

  - <span data-ttu-id="b9cc2-115">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="b9cc2-115">**UpdateCriteria**</span></span>

  - <span data-ttu-id="b9cc2-116">**Reshape Name**</span><span class="sxs-lookup"><span data-stu-id="b9cc2-116">**Reshape Name**</span></span>

  - <span data-ttu-id="b9cc2-117">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="b9cc2-117">**AutoRecalc**</span></span>

<span data-ttu-id="b9cc2-p101">Diese Eigenschaften werden im Schemaabschnitt als Attribute der Elementdefinition für das **Recordset** -Objekt gespeichert. Diese Attribute werden im Rowsetschemanamespace definiert und müssen das Präfix "rs:" enthalten.</span><span class="sxs-lookup"><span data-stu-id="b9cc2-p101">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted. These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

