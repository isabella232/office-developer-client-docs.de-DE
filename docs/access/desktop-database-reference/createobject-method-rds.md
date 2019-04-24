---
title: CreateObject-Methode (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ad61495bcc96b3099af6273796626e9442cbf0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295373"
---
# <a name="createobject-method-rds"></a>CreateObject-Methode (RDS)

**Gilt für**: Access 2013, Office 2013

Erstellt den Proxy für das Zielgeschäftsobjekt und gibt einen Zeiger auf das Objekt zurück. Der Proxy verpackt Daten und leitet diese Daten an den serverseitigen Stub für die Kommunikation mit dem Geschäftsobjekt weiter, damit Anfragen und Daten über das Internet gesendet werden. Bei In-Process-Komponentenobjekten werden keine Proxies verwendet, sondern wird lediglich ein Zeiger auf das Objekt bereitgestellt.

## <a name="syntax"></a>Syntax

Von Remote Data Service werden die folgenden Protokolle unterstützt: HTTP, HTTPS (HTTP über Secure Socket Layer), DCOM und In-Process (prozessinternes Protokoll).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Protokoll</p></th>
<th><p>Syntax</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>HTTP</p></td>
<td><p><em>Objekt</em> = -Daten<em>Bereich</em>festlegen. CreateObject (&quot;<em>ProgID</em>&quot; &quot; <em>https://awebsrvr</em>, &quot;)</p></td>
</tr>
<tr class="even">
<td><p>HTTPS</p></td>
<td><p><em>Objekt</em> = -Daten<em>Bereich</em>festlegen. CreateObject (&quot;<em>ProgID</em>&quot; &quot; <em>https://awebsrvr</em>, &quot;)</p></td>
</tr>
<tr class="odd">
<td><p>DCOM</p></td>
<td><p><em>Objekt</em> = -Daten<em>Bereich</em>festlegen. CreateObject (&quot;<em>ProgID</em>&quot;, &quot; <em>Computername</em>&quot;)</p></td>
</tr>
<tr class="even">
<td><p>In-Process</p></td>
<td><p><em>Objekt</em> = -Daten<em>Bereich</em>festlegen. CreateObject (&quot;<em>ProgID</em>&quot;, &quot; &quot;)</p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Objekt* |Eine Objektvariable, die zu einem Objekt ausgewertet wird, das den in *ProgID* angegebenen Typ hat.|
|*DataSpace* |Eine Objektvariable, die ein [RDS.DataSpace](dataspace-object-rds.md)-Objekt darstellt, das zum Erstellen einer Instanz des neuen Objekts verwendet wird.|
|*ProgID* |Ein **String** -Wert mit dem programmgesteuerten Bezeichner, der ein serverseitiges Geschäftsobjekt angibt, das die Geschäftregeln Ihrer Anwendung implementiert.|
|*awebsrvr* oder *Computername* |Ein **String** -Wert, der eine URL darstellt, die den Internetinformationsdienste-Webserver (IIS) angibt, auf dem eine Instanz des Server Geschäftsobjekts erstellt wird.|

## <a name="remarks"></a>Bemerkungen

Das *http-Protokoll* ist das standardmäßige Webprotokoll. *Https* ist ein sicheres Webprotokoll. Verwenden Sie das *DCOM-Protokoll* , wenn Sie ein lokales Netzwerk ohne http betreiben. Das *in-Process* -Protokoll ist eine lokale Dynamic Link Library (dll); Es wird kein Netzwerk verwendet.

