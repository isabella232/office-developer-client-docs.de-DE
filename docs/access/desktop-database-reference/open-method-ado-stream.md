---
title: Open-Methode (Stream in ADO)
TOCTitle: Open method (ADO Stream)
ms:assetid: fa2e6aaa-e9f5-009c-f3a0-050a00abf9b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250275(v=office.15)
ms:contentKeyID: 48548833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: cd552046c488d65546ecb83e04b8d7b6047c481f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562580"
---
# <a name="open-method-ado-stream"></a>Open-Methode (Stream in ADO)


**Gilt für**: Access 2013, Office 2013


Öffnet ein [Stream](stream-object-ado.md)-Objekt, um Datenströme von Binär- oder Textdaten zu ändern.

## <a name="syntax"></a>Syntax

*Stream*. Open *Source*, *Mode*, *OpenOptions*, *UserName*, *Password*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Source* |Optional. Ein **Variant**-Wert, der die Datenquelle für das **Stream**-Objekt angibt. *Die Quelle* kann eine absolute URL-Zeichenfolge enthalten, die auf einen vorhandenen Knoten in einer bekannten Struktur verweist, z. B. eine E-Mail oder ein Dateisystem. Eine URL sollte mithilfe des URL-Schlüsselworts ("URL=*Schema*:// / *Serverordner")* angegeben werden. Als Alternative kann *Source* einen Verweis auf ein bereits geöffnetes [Record](record-object-ado.md)-Objekt enthalten, das den dem **Record** zugeordneten Standarddatenstrom öffnet. Ist *Source* nicht angegeben, wird ein **Stream**-Objekt instanziiert und geöffnet, das standardmäßig keiner zugrunde liegenden Quelle zugeordnet ist. Weitere Informationen zu URL-Schemas und den zugehörigen Anbietern finden Sie unter [Absolute und relative URLs.](absolute-and-relative-urls.md)|
|*Mode* |Optional. Ein [ConnectModeEnum](connectmodeenum.md)-Wert, der den Zugriffsmodus für das resultierende **Stream**-Objekt angibt (z. B. Lese-/Schreibzugriff oder schreibgeschützt). Der Standardwert lautet **adModeUnknown**. Weitere Informationen zu Zugriffmodi erhalten Sie unter [Mode](mode-property-ado.md)-Eigenschaft. Ist *Mode* nicht angegeben, wird diese Methode vom Quellobjekt geerbt. Wenn der Quell-**Record** im schreibgeschützten Modus geöffnet ist, wird das **Stream**-Objekt standardmäßig auch im schreibgeschützten Modus geöffnet.|
|*OpenOptions* |Optional. Ein [StreamOpenOptionsEnum](streamopenoptionsenum.md)-Wert. Der Standardwert lautet **adOpenStreamUnspecified**.|
|*UserName* |Optional. Ein **String** -Wert mit der Benutzeridentifikation, mit der bei Bedarf auf das **Stream** -Objekt zugegriffen wird.|
|*Password* |Optional. Ein **String** -Wert, der das Kennwort enthält, mit dem bei Bedarf auf das **Stream** -Objekt zugegriffen wird.|

## <a name="remarks"></a>HinwBemerkungeneise

Wenn ein **Record**-Objekt als Quellparameter übergeben wird, werden die Parameter *UserID* und *Password* nicht verwendet, da der Zugriff auf das **Record**-Objekt bereits vorhanden ist. Der [Mode](mode-property-ado.md) des **Record**-Objekts wird ebenso auf das **Stream**-Objekt übertragen. Ist *Source* nicht angegeben, enthält das geöffnete **Stream**-Objekt keine Daten und weist eine [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) von 0 (Null) auf. Wenn Sie vermeiden möchten, dass beim Schließen des **Stream**-Objekts Daten verlorengehen, die in dieses **Stream**-Objekt geschrieben wurden, speichern Sie das **Stream**-Objekt mit der [CopyTo](copyto-method-ado.md)-Methode oder der [SaveToFile](savetofile-method-ado.md)-Methode, oder speichern Sie ihn an einem anderen Speicherort.

Ein *OpenOptions*-Wert **adOpenStreamFromRecord** identifiziert den Inhalt des *Source*-Parameters als ein bereits offenes **Record**-Objekt. Beim Standardverhalten wird *Source* wie eine URL behandelt, die direkt auf einen Knoten in einer Baumstruktur verweist (z. B. auf eine Datei). Der diesem Knoten zugeordnete Standarddatenstrom wird geöffnet.

Alle schreibgeschützten Eigenschaften des **Stream**-Objekts können selbst dann gelesen werden, wenn das **Stream**-Objekt nicht offen ist. Ist ein **Stream**-Objekt asynchron geöffnet, werden alle nachfolgenden Vorgänge (außer dem Überprüfen des [State](state-property-ado.md) und anderer Eigenschaften) blockiert, bis der **Open**-Vorgang abgeschlossen ist.

Zusätzlich zu den oben beschriebenen Optionen können Sie, indem Sie *"Source"* nicht angeben, einfach ein **Stream-Objekt** im Speicher instanziieren, ohne es einer zugrunde liegenden Quelle zuzuordnen. Sie können dem Datenstrom Daten dynamisch hinzufügen, indem Sie mit **Write** oder [WriteText](write-method-ado.md) einfach Binär- oder Textdaten in das [Stream](writetext-method-ado.md) -Objekt schreiben, oder indem Sie mithilfe von [LoadFromFile](loadfromfile-method-ado.md) Daten aus einer Datei laden.

