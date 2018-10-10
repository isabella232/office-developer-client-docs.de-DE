---
title: Dynamische Eigenschaften des Recordset-Objekts in XML
TOCTitle: Recordset Dynamic Properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4193220e450c59e7293ed6befa37d8da23801f27
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472982"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="6e36a-102">Dynamische Eigenschaften des Recordset-Objekts in XML</span><span class="sxs-lookup"><span data-stu-id="6e36a-102">Recordset Dynamic Properties in XML</span></span>


<span data-ttu-id="6e36a-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e36a-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="6e36a-104">Dynamische Eigenschaften des Recordset-Objekts in XML</span><span class="sxs-lookup"><span data-stu-id="6e36a-104">Recordset Dynamic Properties in XML</span></span>

<span data-ttu-id="6e36a-105">Die folgenden anbieterspezifischen Eigenschaften des **Recordset** -Objekts (im Client Cursor Engine) werden derzeit im XML-Format gespeichert:</span><span class="sxs-lookup"><span data-stu-id="6e36a-105">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

  - <span data-ttu-id="6e36a-106">**Update Resync**</span><span class="sxs-lookup"><span data-stu-id="6e36a-106">**Update Resync**</span></span>

  - <span data-ttu-id="6e36a-107">**Unique Table**</span><span class="sxs-lookup"><span data-stu-id="6e36a-107">**Unique Table**</span></span>

  - <span data-ttu-id="6e36a-108">**Unique Schema**</span><span class="sxs-lookup"><span data-stu-id="6e36a-108">**Unique Schema**</span></span>

  - <span data-ttu-id="6e36a-109">**Unique Catalog**</span><span class="sxs-lookup"><span data-stu-id="6e36a-109">**Unique Catalog**</span></span>

  - <span data-ttu-id="6e36a-110">**Resync Command**</span><span class="sxs-lookup"><span data-stu-id="6e36a-110">**Resync Command**</span></span>

  - <span data-ttu-id="6e36a-111">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="6e36a-111">**IRowsetChange**</span></span>

  - <span data-ttu-id="6e36a-112">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="6e36a-112">**IRowsetUpdate**</span></span>

  - <span data-ttu-id="6e36a-113">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="6e36a-113">**CommandTimeout**</span></span>

  - <span data-ttu-id="6e36a-114">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="6e36a-114">**BatchSize**</span></span>

  - <span data-ttu-id="6e36a-115">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="6e36a-115">**UpdateCriteria**</span></span>

  - <span data-ttu-id="6e36a-116">**Reshape Name**</span><span class="sxs-lookup"><span data-stu-id="6e36a-116">**Reshape Name**</span></span>

  - <span data-ttu-id="6e36a-117">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="6e36a-117">**AutoRecalc**</span></span>

<span data-ttu-id="6e36a-p101">Diese Eigenschaften werden im Schemaabschnitt als Attribute der Elementdefinition für das **Recordset** -Objekt gespeichert. Diese Attribute werden im Rowsetschemanamespace definiert und müssen das Präfix "rs:" enthalten.</span><span class="sxs-lookup"><span data-stu-id="6e36a-p101">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted. These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

