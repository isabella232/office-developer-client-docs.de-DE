---
title: CopyRecord-Methode (ADO)
TOCTitle: CopyRecord Method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a54cf5f4d14b3e623a576dee99e1fabeb070e25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474397"
---
# <a name="copyrecord-method-ado"></a>CopyRecord-Methode (ADO)


**Betrifft**: Access 2013 | Office 2013

Kopiert eine durch einen **Record** dargestellte Entität an einen anderen Speicherort.

## <a name="syntax"></a>Syntax

*Datensatz*. CopyRecord (*Quelle*, *Ziel*, *Benutzername*, *Kennwort*, *Optionen*, *Async*)

## <a name="parameters"></a>Parameter

  - *Source*

  - Optional. Ein **String** -Wert, der eine URL, die Entität kopiert werden soll (beispielsweise eine Datei oder ein Verzeichnis) enthält. Wenn *Source* ausgelassen wird oder eine leere Zeichenfolge angibt, wird die Datei oder das Verzeichnis vom aktuellen [Datensatz](record-object-ado.md) dargestellt kopiert werden.

  - *Destination*

  - Optional. Ein **String** -Wert, der eine URL des Speicherorts, in dem *Quelle* kopiert werden, enthält.

  - *UserName*

  - Optional. Ein **String**-Wert mit der Benutzer-ID, die bei Bedarf Zugriff auf die *Destination* gewährt.

  - *Password*

  - Optional. Ein **String**-Wert, der das Kennwort enthält, das bei Bedarf den *UserName* bestätigt.

  - *Options*

  - Optional. Ein [CopyRecordOptionsEnum](copyrecordoptionsenum.md)-Wert, der den Standardwert **adCopyUnspecified** besitzt. Gibt das Verhalten dieser Methode an.

  - *Async*

  - Optional. Ein **Boolean** -Wert, der im Fall von **True** angibt, dass dieser Vorgang asynchron sein soll.

## <a name="return-value"></a>Rückgabewert

Ein **String**-Wert, der in der Regel den Wert für *Destination* zurückgibt. Der genaue Wert, der zurückgegeben wird, ist jedoch vom Anbieter abhängig.

## <a name="remarks"></a>Hinweise

Die Werte der *Quell-* und *Zielserver* dürfen nicht identisch sein; andernfalls tritt ein Laufzeitfehler. Mindestens einer der Server-, Pfad- oder Ressourcennamen muss unterschiedlich sein.

Wenn **adCopyNonRecursive** nicht angegeben ist, werden alle untergeordneten Ebenen (z. B. Unterverzeichnisse) von *Source* rekursiv kopiert. Bei einem rekursiven Vorgang darf es sich bei der *Destination* nicht um ein Unterverzeichnis von *Source* handeln, andernfalls kann der Vorgang nicht abgeschlossen werden.

Diese Methode schlägt fehl, wenn das *Ziel* eine vorhandene Entität (beispielsweise eine Datei oder ein Verzeichnis) identifiziert, es sei denn, **AdCopyOverWrite** angegeben ist.


> [!IMPORTANT]
> <P>[!WICHTIG] Verwenden Sie die Option <STRONG>adCopyOverWrite</STRONG> nur nach sorgfältiger Überlegung. Beispielsweise wird durch das Angeben dieser Option beim Kopieren einer Datei in ein Verzeichnis das Verzeichnis wird <EM>Löschen</EM> und Ersetzen Sie ihn mit der Datei.</P>




> [!NOTE]
> <P>[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider für Internet Publishing</A> automatisch aufgerufen. Weitere Informationen erhalten Sie unter <A href="absolute-and-relative-urls.md">Absolute und relative URLs</A>.</P>


