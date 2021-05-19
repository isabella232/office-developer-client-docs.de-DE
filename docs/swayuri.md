---
title: SwayURI
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11daa75b-87fc-4e63-8e02-09ab9307c8f8
ms.date: 01/28/2016
description: Verwenden Sie das Sway-URI-Schema, um die Sway-Anwendung zu öffnen und einen Sway zu anzeigen oder zu bearbeiten.
ms.openlocfilehash: 04848ef1de2777d916d8dd8dd381e6d5f66310d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415313"
---
# <a name="sway-uri-scheme"></a>Sway-URI-Schema

In diesem Dokument wird das Format der UNIFORM Resource Identifiers (URIs) für die Sway-Anwendung für Windows. Mit diesem URI-Schema können Sie die Sway-Anwendung mit verschiedenen Befehlen aufrufen.

## <a name="sway-uri-scheme-syntax"></a>Syntax des Sway-URI-Schemas

Im Folgenden finden Sie die Syntax des URI-Schemas:

`<ms-sway>:<command-argument>`

- `<ms-sway>`&ndash;Gibt an, dass Sway die anwendung ist, die aufgerufen werden soll. Wenn Sway für Windows installiert ist, wird bei Windows als `ms-sway` Sway-Handler registriert.
- `<command-argument>`&ndash;Ein URI kann ein oder mehrere Befehlsargumente haben, die durch das Zeichen ampersand ( `&` ) getrennt sind. Wenn mehrere Befehlsargumente in einem URI enthalten sind, muss jedes Befehlsargument durch ein kaufmännisches und ( ) Zeichen vom folgenden `&` Befehlsargument getrennt werden. Befehlsargumente variieren je nach Szenario. 

## <a name="command-arguments"></a>Befehlsargumente

Mehrere Befehlsargumente können als Teil des Sway-URL-Schemas eingeschlossen werden. Diese Befehlsargumente sind nicht erforderlich. Wenn Sie die Befehlsargumente nicht enthalten, wird die Sway-Anwendung aufgerufen.

|Name des Command-Arguments|Beschreibung|Typ|Mögliche Werte|Pflichtfeld?|
|:-----|:-----|:-----|:-----|:-----|
|**id**|Der eindeutige Bezeichner eines Sway. Wird verwendet, um den zu öffnende Sway anzugeben.|String|Ein gültiger eindeutiger Bezeichner für einen Sway. Die ID ist immer Teil der URL zu einem Sway.<br/><br/>Für den folgenden Sway ist `https://sway.com/dBheQgVZ1RQBfiQU` z. B. die ID `dBheQgVZ1RQBfiQU` .<br/><br/>Wenn das der Sway-Anwendung zugeordnete Benutzerkonto über Bearbeitungsberechtigungen verfügt, öffnet die Anwendung den Sway im Bearbeitungsmodus. Andernfalls öffnet die Anwendung den Sway im Ansichtsmodus.|Nein|
|**mode**|Der Modus, in dem ein bestimmter Sway geöffnet werden soll, unabhängig davon, ob er bearbeitet oder angezeigt werden soll.|String|Bearbeiten<br/>Ansicht<br/><br/>**HINWEIS**: Wenn keine **ID** angegeben ist, wird dieses Befehlsargument ignoriert.|Nein|
|**auth_upn**|Das Konto, das beim Öffnen von Sway verwendet werden soll.|String|Eine gültige E-Mail-Adresse.<br/><br/>Wenn die angegebene E-Mail-Adresse keinem Sway-Konto zugeordnet ist, fordert Sway den Benutzer auf, sich als angegebener Benutzer zu registrieren.<br/><br/>Wenn der Sway-Anwendung mehr als ein Konto zugeordnet ist und die angegebene E-Mail-Adresse vorhanden ist, wechselt die Sway-Anwendung beim Aufrufen zu verwendung dieses Kontos.|Nein|
|**auth \_ pvr**|Der Typ des Kontos, das verwendet werden soll, um das Sway entweder ein Microsoft-Konto oder ein Azure Active Directory &mdash; (Azure AD) zu öffnen.|String|WindowsLiveId – Gibt an, dass es sich bei dem **\_ Authentifizierungskonto** um ein Microsoft-Konto handelt.<br/><br/>OrgId – Gibt an, dass es sich bei dem **\_ Authentifizierungskonto** um ein Azure AD-Konto handelt.<br/><br/>Wenn kein **\_ Authentifizierungs-Upn** angegeben ist, wird dieses Befehlsargument ignoriert.|Nein|
|**Aufrufen der \_ App**|Der Name der Windows, die zum Aufrufen von Sway verwendet wird.|String|Der Anzeigename der Windows, die zum Aufrufen von Sway über das Sway-URL-Schema verwendet wird.<br/><br/>Dieses Befehlsargument dient der Telemetrie und Nachverfolgung.|Nein|

## <a name="uri-scheme-semantics"></a>URI-Schemasemantik

Das Schema definiert eine #A0 zum Öffnen eines Sway oder zum Aufrufen `<ms-sway>` der Sway-Anwendung. Das Schema definiert mehrere Befehlsargumente, die für folgende Aufgaben verwendet werden können: 

- Öffnen Sie die Sway-Anwendung &ndash; Keine Befehlsargumente müssen angegeben werden. 

- Öffnen Sie einen Sway zum Anzeigen in der Sway-Anwendung Die id und der Modus, der für die Anzeige &ndash; festgelegt ist, müssen angegeben werden.   

- Öffnen Sie ein Sway zur Bearbeitung in der Sway-Anwendung Die ID und der modus, der für die Bearbeitung &ndash; festgelegt ist, müssen angegeben werden.   Es wird empfohlen, dass Sie auch **\_ Authentifizierungs-** und Authentifizierungs-pvr verwenden, um sicherzustellen, dass beim Öffnen von Sway das richtige Konto mit Bearbeitungsberechtigungen verwendet wird. **\_**  

## <a name="example"></a>Beispiel

`ms-sway:id=CyrvEYLmFKi1B2_I&auth_upn=account@email.com&auth_pvr=WindowsLiveId&invoking_app=MyApp` 


