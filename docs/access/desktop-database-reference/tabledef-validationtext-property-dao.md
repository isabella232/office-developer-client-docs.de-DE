---
title: TableDef.ValidationText Property (DAO)
TOCTitle: ValidationText Property
ms:assetid: 9f38616a-41ee-cbd1-9e29-da436b258e08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198366(v=office.15)
ms:contentKeyID: 48546682
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9b39f263786dafd23234747f72f5e289a2350e1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472653"
---
# <a name="tabledefvalidationtext-property-dao"></a><span data-ttu-id="81156-102">TableDef.ValidationText Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="81156-102">TableDef.ValidationText Property (DAO)</span></span>


<span data-ttu-id="81156-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="81156-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="81156-p101">Legt einen Wert fest, der den Text der Nachricht angibt, die von der Anwendung angezeigt wird, wenn der Wert eines **Field**-Objekts die von der **ValidationRule**-Eigenschaft festgelegte Gültigkeitsregel nicht unterstützt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="81156-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="81156-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="81156-106">Syntax</span></span>

<span data-ttu-id="81156-107">*Ausdruck* . ValidationText</span><span class="sxs-lookup"><span data-stu-id="81156-107">*expression* .ValidationText</span></span>

<span data-ttu-id="81156-108">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="81156-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="81156-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81156-109">Remarks</span></span>

<span data-ttu-id="81156-110">Bei einem **[TableDef](tabledef-object-dao.md)** -Objekt ist der Wert dieser Eigenschaft für eine verknüpfte Tabelle schreibgeschützt. Für eine Basistabelle besteht Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="81156-110">For a **[TableDef](tabledef-object-dao.md)** object, this property setting is read-only for a linked table and read/write for a base table.</span></span>

