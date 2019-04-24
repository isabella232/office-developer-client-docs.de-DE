---
title: CopyRecord-Methode (ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5aac745bacf0662f6cd389bfefde7182a9676d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295527"
---
# <a name="copyrecord-method-ado"></a>CopyRecord-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Kopiert eine durch einen **Record** dargestellte Entität an einen anderen Speicherort.

## <a name="syntax"></a>Syntax

*Record*. CopyRecord (*Quelle*, *Ziel*, *Benutzername*, *Kennwort*, *Optionen*, *Async*)

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Source* |Optional. Ein **String**-Wert mit einer URL, die die zu kopierende Entität (z. B. eine Datei oder ein Verzeichnis) angibt. Wenn *Source* nicht angegeben ist oder eine leere Zeichenfolge angibt, wird die bzw. das durch den aktuellen [Record](record-object-ado.md) dargestellte Datei oder Verzeichnis kopiert.|
|*Destination* |Optional. Ein **String**-Wert mit einer URL, die den Speicherort angibt, an den die *Source* kopiert werden soll.|
|*UserName* |Optional. Ein **String**-Wert mit der Benutzer-ID, die bei Bedarf Zugriff auf die *Destination* gewährt.|
|*Password* |Optional. Ein **String**-Wert, der das Kennwort enthält, das bei Bedarf den *UserName* bestätigt.|
|*Options* |Optional. Ein [CopyRecordOptionsEnum](copyrecordoptionsenum.md)-Wert, der den Standardwert **adCopyUnspecified** besitzt. Gibt das Verhalten dieser Methode an.|
|*Async* |Optional. Ein **Boolean** -Wert, der im Fall von **True** angibt, dass dieser Vorgang asynchron sein soll.|

## <a name="return-value"></a>Rückgabewert

Ein **String**-Wert, der in der Regel den Wert für *Destination* zurückgibt. Der genaue Wert, der zurückgegeben wird, ist jedoch vom Anbieter abhängig.

## <a name="remarks"></a>Bemerkungen

Die Werte für *Source* und *Destination* dürfen nicht identisch sein, andernfalls tritt ein Laufzeitfehler auf. Mindestens einer der Server-, Pfad- oder Ressourcennamen muss unterschiedlich sein.

Wenn **adCopyNonRecursive** nicht angegeben ist, werden alle untergeordneten Ebenen (z. B. Unterverzeichnisse) von *Source* rekursiv kopiert. Bei einem rekursiven Vorgang darf es sich bei der *Destination* nicht um ein Unterverzeichnis von *Source* handeln, andernfalls kann der Vorgang nicht abgeschlossen werden.

Diese Methode schlägt fehl, wenn die *Destination* eine vorhandene Entität (z. B. eine Datei oder ein Verzeichnis) angibt und **adCopyOverWrite** nicht angegeben ist.

> [!IMPORTANT]
> Verwenden Sie die Option **adCopyOverWrite** nur nach sorgfältiger Überlegung. Wenn Sie diese Option beispielsweise beim Kopieren einer Datei in ein Verzeichnis angeben, wird das Verzeichnis *gelöscht* und durch die Datei ersetzt.


> [!NOTE]
> Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen. Weitere Informationen finden Sie unter [absolute und relative URLs](absolute-and-relative-urls.md).


