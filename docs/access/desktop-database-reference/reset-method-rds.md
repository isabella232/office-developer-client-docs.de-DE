---
title: Reset-Methode (RDS - Access-desktop-Datenbank (engl.))
TOCTitle: Reset method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 898045bcfdd3fb2483954155319e6aab3d0ebc7f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714240"
---
# <a name="reset-method-rds"></a>Reset-Methode (RDS)

**Betrifft**: Access 2013, Office 2013

Führt auf der Grundlage der angegebenen Eigenschaften zum Sortieren und Filtern die Sortierung und Filterung für ein clientseitiges **Recordset** -Objekt aus.

## <a name="syntax"></a>Syntax

*DataControl*. Zurücksetzen (*Wert*)

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DataControl* |Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|
|*Value* |Optional. Ein **Boolean** -Wert, der **True** (Standardeinstellung) ist, wenn Sie das aktuelle "gefilterte" Rowset filtern möchten. **False** gibt an, dass Sie das urspüngliche Rowset filtern, wobei alle vorherigen Filteroptionen entfernt werden.|

## <a name="remarks"></a>Hinweise

Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) und [FilterColumn](filtercolumn-property-rds.md) bieten Funktionalitäten zum Filtern im clientseitigen Cache. Die Funktion zum Sortieren fordert aus einer Spalte Datensätze nach Werten an. Die Funktion zum Filtern zeigt auf der Grundlage eines Suchkriteriums eine Teilmenge von Datensätzen an, wobei das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache beibehalten wird. Die **Reset** -Methode führt das Kriterium aus und ersetzt das aktuelle **Recordset** -Objekt durch ein aktualisierbares **Recordset** -Objekt.

Wenn an den ursprünglichen Daten noch nicht übermittelte Änderungen vorgenommen wurde, schlägt die **Reset** -Methode fehl. Verwenden Sie zunächst die [SubmitChanges](submitchanges-method-rds.md)-Methode, um alle Änderungen in einem **Recordset** -Objekt mit Lese-/Schreibzugriff zu speichern, und sortieren oder filtern Sie die Datensätze anschließend mithilfe der **Reset** -Methode.

Wenn Sie mehrere Filter für Ihr Rowset ausführen möchten, können Sie die optionalen verwenden *boolesches* Argument mit der Methode **Zurücksetzen** . Im folgenden Beispiel wird dargestellt, wie Sie dazu vorgehen:

