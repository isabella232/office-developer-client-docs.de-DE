---
title: QueryDef.Updatable-Eigenschaft (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5321e834f1dd5ed663033cacb530962d7beeb5a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713366"
---
# <a name="querydefupdatable-property-dao"></a>QueryDef.Updatable-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann. Schreibgeschützter **Boolean**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . Aktualisierbar

*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die **Updatable**-Eigenschaft eines **QueryDef**-Objekts wird auf **True** gesetzt, wenn die Abfragedefinition aktualisiert werden kann, selbst wenn das sich ergebende **[Recordset](recordset-object-dao.md)** -Objekt nicht aktualisiert werden kann.

