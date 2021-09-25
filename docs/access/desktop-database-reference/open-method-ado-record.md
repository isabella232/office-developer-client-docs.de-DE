---
title: Open-Methode (ADO-Datensatz)
TOCTitle: Open method (ADO Record)
ms:assetid: ba71c5c7-326e-d3b6-0e74-e8343ee6896f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249896(v=office.15)
ms:contentKeyID: 48547371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 87fe3e50c6abc0d78f1bf506c02bc63829fec882
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602115"
---
# <a name="open-method-ado-record"></a>Open-Methode (ADO-Datensatz)

**Gilt für**: Access 2013, Office 2013

Öffnet ein vorhandenes [Record](record-object-ado.md)-Objekt oder erstellt ein neues durch den **Record** dargestelltes Element (z. B. eine Datei oder ein Verzeichnis).

## <a name="syntax"></a>Syntax

Open *Source*, *ActiveConnection*, *Mode*, *CreateOptions*, *Options*, *UserName*, *Password*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Source* |Optional. Ein **Variant** -Wert, der Folgendes darstellt: die URL der durch dieses **Record** -Objekt darzustellenden Entität, einen **Command**, ein offenes [Recordset](recordset-object-ado.md)-Objekt oder ein anderes **Record** -Objekt, eine Zeichenfolge mit einer SQL SELECT-Anweisung oder einen Tabellennamen.|
|*Activeconnection* | Optional. Ein **Variant** -Wert, der die Verbindungszeichenfolge oder das offene [Connection](connection-object-ado.md)-Objekt darstellt.|
|*Mode* |Optional. Ein [ConnectModeEnum](connectmodeenum.md)-Wert, dessen Standardwert **adModeUnknown** ist und der den Zugriffsmodus für das resultierende **Record** -Objekt angibt.|
|*Createoptions* |Optional. Ein [RecordCreateOptionsEnum](recordcreateoptionsenum.md)-Wert, dessen Standardwert **adFailIfNotExists** lautet und der angibt, ob eine vorhandene Datei bzw. ein vorhandenes Verzeichnis geöffnet oder eine neue Datei bzw. ein neues Verzeichnis erstellt werden soll. Ist dieser Wert auf den Standardwert festgelegt, wird der Zugriffsmodus aus der [Mode](mode-property-ado.md)-Eigenschaft abgerufen. Dieser Parameter wird ignoriert, wenn der *Source*-Parameter keine URL enthält.|
|*Options* |Optional. Ein [RecordOpenOptionsEnum](recordopenoptionsenum.md)-Wert, dessen Standardwert **adOpenRecordUnspecified** lautet und der Optionen zum Öffnen des **Record** angibt. Diese Werte können kombiniert werden.|
|*UserName* |Optional. Ein **String**-Wert mit der Benutzer-ID, die bei Bedarf Zugriff auf die *Source* gewährt.|
|*Password* |Optional. Ein **String**-Wert, der das Kennwort enthält, das bei Bedarf den *UserName* bestätigt.|

## <a name="remarks"></a>HinwBemerkungeneise

*Source* kann folgende Elemente darstellen:

- Eine URL. Falls es sich bei dem Protokoll für diese URL um HTTP handelt, wird standardmäßig der Internetanbieter aufgerufen. Verweist die URL auf einen Knoten, der ein ausführbares Skript (z. B. eine ASP-Seite) enthält, wird standardmäßig ein **Record**, das die Quelle enthält, und kein ausführbarer Inhalt geöffnet. Verwenden Sie das Argument *Options*, um dieses Verhalten zu ändern.

- Ein **Record** -Objekt. Ein aus einem anderen **Record** geöffnetes **Record** -Objekt klont das ursprüngliche **Record** -Objekt.

- Ein **Command** -Objekt. Das geöffnete **Record** -Objekt stellt die einzelne Zeile dar, die beim Ausführen des **Command** zurückgegeben wurde. Enthalten die Ergebnisse mehrere Zeilen, wird der Inhalt der ersten Zeile im Datensatz platziert und der **Errors** -Auflistung wird möglicherweise ein Fehler hinzugefügt.

- Eine SQL SELECT-Anweisung. Das geöffnete **Record** -Objekt stellt die einzelne Zeile dar, die beim Ausführen des Inhalts der Zeichenfolge zurückgegeben wird. Enthalten die Ergebnisse mehrere Zeilen, wird der Inhalt der ersten Zeile im Datensatz platziert und der **Errors** -Auflistung wird möglicherweise ein Fehler hinzugefügt.

- Einen Tabellennamen.

Stellt das **Record** -Objekt eine Entität dar, auf die nicht mithilfe einer URL zugegriffen werden kann (z. B. eine Zeile eines aus einer Datenbank abgeleiteten **Recordset** -Objekts), sind die Werte der [ParentURL](parenturl-property-ado.md)-Eigenschaft und des Felds, auf das mit der **adRecordURL** -Konstante zugegriffen wird, gleich 0 (Null).

> [!NOTE]
> [!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der [Microsoft OLE DB Provider für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) automatisch aufgerufen. Weitere Informationen finden Sie unter [Absolute und relative URLs.](absolute-and-relative-urls.md)


