---
title: TableDef.Updatable-Eigenschaft (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 71202203588182ba2bf1ba1449f2b1ee04c82c67
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926199"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="be754-102">TableDef.Updatable-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="be754-102">TableDef.Updatable property (DAO)</span></span>


<span data-ttu-id="be754-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be754-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be754-p101">Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann. Schreibgeschützter **Boolean**-Wert.</span><span class="sxs-lookup"><span data-stu-id="be754-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="be754-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="be754-106">Syntax</span></span>

<span data-ttu-id="be754-107">*Ausdruck* . Aktualisierbar</span><span class="sxs-lookup"><span data-stu-id="be754-107">*expression* .Updatable</span></span>

<span data-ttu-id="be754-108">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="be754-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="be754-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be754-109">Remarks</span></span>

<span data-ttu-id="be754-p102">Die **Updatable**-Eigenschaft für ein neu erstelltes **TableDef**-Objekt ist immer **True** und für ein verknüpftes **TableDef**-Objekt **False**. Ein neues **TableDef**-Objekt kann nur an eine Datenbank angefügt werden, für die der Benutzer Schreibberechtigung besitzt.</span><span class="sxs-lookup"><span data-stu-id="be754-p102">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object. A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>

