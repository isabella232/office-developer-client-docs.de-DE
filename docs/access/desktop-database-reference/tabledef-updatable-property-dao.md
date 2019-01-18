---
title: TableDef.Updatable-Eigenschaft (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6e6c7409b89058c6be55d9fb83eb85c7af9fb9c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725973"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="27896-102">TableDef.Updatable-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="27896-102">TableDef.Updatable property (DAO)</span></span>


<span data-ttu-id="27896-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="27896-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27896-p101">Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann. Schreibgeschützter **Boolean**-Wert.</span><span class="sxs-lookup"><span data-stu-id="27896-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="27896-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="27896-106">Syntax</span></span>

<span data-ttu-id="27896-107">*Ausdruck* . Aktualisierbar</span><span class="sxs-lookup"><span data-stu-id="27896-107">*expression* .Updatable</span></span>

<span data-ttu-id="27896-108">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="27896-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="27896-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27896-109">Remarks</span></span>

<span data-ttu-id="27896-p102">Die **Updatable**-Eigenschaft für ein neu erstelltes **TableDef**-Objekt ist immer **True** und für ein verknüpftes **TableDef**-Objekt **False**. Ein neues **TableDef**-Objekt kann nur an eine Datenbank angefügt werden, für die der Benutzer Schreibberechtigung besitzt.</span><span class="sxs-lookup"><span data-stu-id="27896-p102">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object. A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>

