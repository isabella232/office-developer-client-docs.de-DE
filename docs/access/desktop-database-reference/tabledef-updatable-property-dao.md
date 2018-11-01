---
title: TableDef.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4908699aaea69a001a1abd3761b78607ae2640a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869820"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="f5485-102">TableDef.Updatable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="f5485-102">TableDef.Updatable Property (DAO)</span></span>


<span data-ttu-id="f5485-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5485-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f5485-p101">Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann. Schreibgeschützter **Boolean**-Wert.</span><span class="sxs-lookup"><span data-stu-id="f5485-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5485-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5485-106">Syntax</span></span>

<span data-ttu-id="f5485-107">*Ausdruck* . Aktualisierbar</span><span class="sxs-lookup"><span data-stu-id="f5485-107">*expression* .Updatable</span></span>

<span data-ttu-id="f5485-108">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="f5485-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5485-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5485-109">Remarks</span></span>

<span data-ttu-id="f5485-p102">Die **Updatable**-Eigenschaft für ein neu erstelltes **TableDef**-Objekt ist immer **True** und für ein verknüpftes **TableDef**-Objekt **False**. Ein neues **TableDef**-Objekt kann nur an eine Datenbank angefügt werden, für die der Benutzer Schreibberechtigung besitzt.</span><span class="sxs-lookup"><span data-stu-id="f5485-p102">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object. A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>

