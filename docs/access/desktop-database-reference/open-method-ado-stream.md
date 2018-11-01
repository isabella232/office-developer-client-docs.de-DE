---
title: Open-Methode (Stream in ADO)
TOCTitle: Open Method (ADO Stream)
ms:assetid: fa2e6aaa-e9f5-009c-f3a0-050a00abf9b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250275(v=office.15)
ms:contentKeyID: 48548833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ac01f67bb18ea15959f4b5c09dbe4037da8010bc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883239"
---
# <a name="open-method-ado-stream"></a>Open-Methode (Stream in ADO)


**Betrifft**: Access 2013, Office 2013


Öffnet ein [Stream](stream-object-ado.md)-Objekt, um Datenströme von Binär- oder Textdaten zu ändern.

## <a name="syntax"></a>Syntax

*Stream-Objekt*. Öffnen Sie *Source*, *Modus*, *OpenOptions*, *Benutzername*, *Kennwort*

## <a name="parameters"></a>Parameter

  - *Source*

  - Optional. Ein **Variant** -Wert, der die Quelle der Daten für das **Stream-Objekt**angibt. *Source* kann eine absolute URL-Zeichenfolge enthalten, die auf einem vorhandenen Knoten in einer bekannten Baumstruktur, wie eine e-Mail- oder Dateisystem verweist. Eine URL sollte mithilfe des URL-Schlüsselworts angegeben werden ("URL =*Schema*://*Server*/*Ordner*"). *Quelle* kann auch einen Verweis auf ein bereits geöffnetes [Record](record-object-ado.md) -Objekt enthalten, das den dem **Eintrag**zugeordneten Standarddatenstrom geöffnet wird. Wenn *Source* nicht angegeben wird, ist ein **Stream-Objekt** instanziiert und geöffnet, keine zugrunde liegenden Quelle standardmäßig zugeordnet. Weitere Informationen zu URL-Schemas und deren zugeordneten Anbietern finden Sie unter [Absolute und Relative URLs](absolute-and-relative-urls.md).

  - *Mode*

  - Optional. Eine [ConnectModeEnum](connectmodeenum.md) -Wert, der den Zugriffsmodus für das resultierende **Stream** angibt (beispielsweise Lese-/Schreibzugriff oder schreibgeschützt). Standardwert ist **AdModeUnknown**. Finden Sie unter die [Mode](mode-property-ado.md) -Eigenschaft für Weitere Informationen zu Access-Modi. Wenn der *Authentifizierungsmodus* nicht angegeben ist, wird es von der Source-Objekt geerbt. Beispielsweise, wenn die Quelle **Datensatz** im schreibgeschützten Modus geöffnet wird, wird der **Stream** auch im schreibgeschützten Modus standardmäßig geöffnet werden.

  - *OpenOptions*

  - Optional. Ein [StreamOpenOptionsEnum](streamopenoptionsenum.md)-Wert. Der Standardwert lautet **adOpenStreamUnspecified**.

  - *UserName*

  - Optional. Ein **String** -Wert mit der Benutzeridentifikation, mit der bei Bedarf auf das **Stream** -Objekt zugegriffen wird.

  - *Password*

  - Optional. Ein **String** -Wert, der das Kennwort enthält, mit dem bei Bedarf auf das **Stream** -Objekt zugegriffen wird.

## <a name="remarks"></a>Hinweise

Wenn ein **Record** -Objekts als der Source-Parameter, die *Benutzer-ID* und *das Kennwort* -Parameter übergeben wird werden nicht verwendet werden, da bereits Zugriff auf das **Record** -Objekt zur Verfügung steht. Entsprechend wird der [Modus](mode-property-ado.md) des **Record** -Objekts an das **Stream** -Objekt weitergeleitet. Wenn *Source* nicht angegeben wird, die geöffneten **Stream-Objekt** enthält keine Daten und weist eine [Größe](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) von null (0). Speichern Sie des **Stream-Objekt** mit der [CopyTo](copyto-method-ado.md) oder [SaveToFile](savetofile-method-ado.md) -Methoden vermeiden Verlust von Daten, die in diesen **Stream** geschrieben werden, wenn der **Stream** geschlossen ist, oder auf einen anderen Speicherort zu speichern.

Ein Wert *OpenOptions* **adOpenStreamFromRecord** identifiziert den Inhalt des *Source* -Parameter ein bereits geöffnetes **Record** -Objekt sein. Das Standardverhalten besteht, *Datenquelle* als eine URL zu behandeln, die direkt auf einen Knoten in einer Baumstruktur, wie etwa einer Datei verweist. Der diesem Knoten zugeordnete Standarddatenstrom wird geöffnet.

Alle schreibgeschützten Eigenschaften des **Stream** -Objekts können selbst dann gelesen werden, wenn das **Stream** -Objekt nicht offen ist. Ist ein **Stream** -Objekt asynchron geöffnet, werden alle nachfolgenden Vorgänge (außer dem Überprüfen des [State](state-property-ado.md) und anderer Eigenschaften) blockiert, bis der **Open** -Vorgang abgeschlossen ist.

Zusätzlich zu den oben beschrieben, durch angeben nicht *Quelle*Optionen, können Sie einfach ein **Stream** -Objekt im Speicher instanziieren, ohne eine zugrunde liegende Datenquelle zuzuordnen. Sie können dem Datenstrom Daten dynamisch hinzufügen, indem Sie mit **Write** oder [WriteText](write-method-ado.md) einfach Binär- oder Textdaten in das [Stream](writetext-method-ado.md) -Objekt schreiben, oder indem Sie mithilfe von [LoadFromFile](loadfromfile-method-ado.md) Daten aus einer Datei laden.

