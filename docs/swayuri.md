---
title: SwayURI
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11daa75b-87fc-4e63-8e02-09ab9307c8f8
ms.date: 01/28/2016
description: Verwenden Sie das Sway-URI-Schema, um die Sway-Anwendung zu öffnen und eine Sway anzuzeigen oder zu bearbeiten.
ms.openlocfilehash: 04848ef1de2777d916d8dd8dd381e6d5f66310d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415313"
---
# <a name="sway-uri-scheme"></a>Sway-URI-Schema

Dieses Dokument definiert das Format von Uniform Resource Identifier (URIs) für die Sway-Anwendung für Windows. Sie können dieses URI-Schema verwenden, um die Sway-Anwendung mit verschiedenen Befehlen aufzurufen.

## <a name="sway-uri-scheme-syntax"></a>Syntax für das Sway-URI-Schema

Es folgt die Syntax des URI-Schemas:

`<ms-sway>:<command-argument>`

- `<ms-sway>`&ndash; Gibt an, dass Sway die Anwendung ist, die aufgerufen werden soll. Wenn Sway for Windows installiert ist, `ms-sway` wird mit Windows als der Sway-Handler registriert.
- `<command-argument>`&ndash; Ein URI kann über ein oder mehrere Befehlsargumente verfügen, die durch das kaufmännische`&`und-Zeichen () begrenzt werden. Wenn in einem URI mehr als ein Command-Argument enthalten ist, muss ein`&`kaufmännisches und-Zeichen () jedes Befehlsargument vom folgenden Befehlsargument trennen. Befehlsargumente variieren je nach Szenario. 

## <a name="command-arguments"></a>Befehlsargumente

Mehrere Befehlsargumente können als Teil des Sway-URL-Schemas eingeschlossen werden. Diese Befehlsargumente sind nicht erforderlich. Wenn Sie die Befehlsargumente nicht angeben, wird die Sway-Anwendung aufgerufen.

|Name des Befehlsarguments|Beschreibung|Typ|Mögliche Werte|Pflichtfeld?|
|:-----|:-----|:-----|:-----|:-----|
|**id**|Der eindeutige Bezeichner eines Sway. Wird verwendet, um die zu öffnende Sway anzugeben.|String|Ein gültiger eindeutiger Bezeichner für eine Sway. Die ID ist immer Teil der URL zu einem Sway.<br/><br/>Beispielsweise ist `dBheQgVZ1RQBfiQU`die ID für die `https://sway.com/dBheQgVZ1RQBfiQU`folgende Sway.<br/><br/>Wenn das mit der Sway-Anwendung verknüpfte Benutzerkonto über Bearbeitungsberechtigungen verfügt, öffnet die Anwendung die Sway im Bearbeitungsmodus. Andernfalls öffnet die Anwendung die Sway im Ansichtsmodus.|Nein|
|**mode**|Der Modus, in dem eine bestimmte Sway geöffnet werden soll, sei es zur Bearbeitung oder zur Anzeige.|String|Bearbeiten<br/>Ansicht<br/><br/>**Hinweis**: Wenn keine **ID** angegeben wird, wird dieses Befehlsargument ignoriert.|Nein|
|**auth_upn**|Das Konto, das beim Öffnen von Sway verwendet werden soll.|String|Eine gültige e-Mail-Adresse.<br/><br/>Wenn die angegebene e-Mail-Adresse keinem Sway-Konto zugeordnet ist, fordert Sway den Benutzer auf, sich als der angegebene Benutzer anzumelden.<br/><br/>Wenn der Sway-Anwendung mehr als ein Konto zugeordnet ist und die angegebene e-Mail-Adresse vorhanden ist, wechselt die Sway-Anwendung zur Verwendung dieses Kontos, wenn Sie aufgerufen wird.|Nein|
|**auth\_PVR**|Der Kontotyp, der zum Öffnen der Sway&mdash;verwendet werden soll, entweder ein Microsoft-Konto oder ein Azure Active Directory-Konto (Azure AD).|String|WindowsLiveId – gibt an, dass das **auth\_-UPN** -Konto ein Microsoft-Konto ist.<br/><br/>OrgId – gibt an, dass das **auth\_-UPN** -Konto ein Azure AD-Konto ist.<br/><br/>Wenn kein **auth\_-UPN** angegeben wird, wird dieses Befehlsargument ignoriert.|Nein|
|**Aufrufen\_der APP**|Der Name der Windows-Anwendung, die zum Aufrufen von Sway verwendet wurde.|String|Der Anzeigename der Windows-Anwendung, die verwendet wird, um Sway über das Sway-URL-Schema aufzurufen.<br/><br/>Der Zweck dieses Befehlsarguments ist die Telemetrie und Nachverfolgung.|Nein|

## <a name="uri-scheme-semantics"></a>URI-Schema Semantik

Das `<ms-sway>` Schema definiert eine URI-Syntax zum Öffnen einer Sway oder zum Aufrufen der Sway-Anwendung. Das Schema definiert mehrere Befehlsargumente, die für folgende Aufgaben verwendet werden können: 

- Öffnen der Sway- &ndash; Anwendung es müssen keine Befehlsargumente angegeben werden. 

- Öffnen Sie eine Sway für die Anzeige in der &ndash; Sway **-** Anwendung die ID und der **Modus** , die angezeigt werden sollen, müssen angegeben werden. 

- Öffnen Sie ein Sway zur Bearbeitung in der Sway &ndash; -Anwendung die **ID** und der **Modus** , die auf Bearbeiten festgelegt sind, müssen angegeben werden. Es wird empfohlen, dass Sie **auch\_auth UPN** und **auth\_PVR** hinzufügen, um sicherzustellen, dass das richtige Konto mit Bearbeitungsberechtigungen verwendet wird, wenn Sway geöffnet wird.  

## <a name="example"></a>Beispiel

`ms-sway:id=CyrvEYLmFKi1B2_I&auth_upn=account@email.com&auth_pvr=WindowsLiveId&invoking_app=MyApp` 


