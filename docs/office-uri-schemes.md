---
title: Office-URI-Schemas
manager: luken
ms.date: 01/14/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ea99a8f-b005-4b92-b313-923294d20fbf
ms.openlocfilehash: 834c4d2c2f47c6cc3f35423a7dfe3c13caf3d209
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790900"
---
# <a name="office-uri-schemes"></a><span data-ttu-id="ea8cf-102">Office-URI-Schemas</span><span class="sxs-lookup"><span data-stu-id="ea8cf-102">Office URI Schemes</span></span>

## <a name="11-abstract"></a><span data-ttu-id="ea8cf-103">1.1 EXPOSEE</span><span class="sxs-lookup"><span data-stu-id="ea8cf-103">1.1 ABSTRACT</span></span>

<span data-ttu-id="ea8cf-p101">Dieses Dokument definiert das Format von Uniform Resource Identifiers (URIs) für Office-Produktivitätsanwendungen. Das Schema wird in Microsoft Office 2010 Service Pack 2 und höher unterstützt, z. B. in den Microsoft Office 2013-Produkten für Windows und den Microsoft SharePoint 2013-Produkten. Es wird auch in Office für iPhone, Office für iPad und Office für Mac 2011 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p101">This document defines the format of Uniform Resource Identifiers (URIs) for office productivity applications. The scheme is supported in Microsoft Office 2010 Service Pack 2 and later, including the Microsoft Office 2013 for Windows and the Microsoft SharePoint 2013 products. It is also supported in Office for iPhone, Office for iPad, and Office for Mac 2011.</span></span>
  
## <a name="12-introduction"></a><span data-ttu-id="ea8cf-107">1.2 EINFÜHRUNG</span><span class="sxs-lookup"><span data-stu-id="ea8cf-107">1.2 INTRODUCTION</span></span>

<span data-ttu-id="ea8cf-p102">Dank dieser URI-Schemas können Office-Produktivitätsanwendungen mit verschiedenen Befehlen aufgerufen werden. Jede Anwendung erhält ein anders benanntes Schema, aber in allen Schemas gelten dieselben Regeln für den Aufbaus des URI (URI-Schema).</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p102">These URI schemes allow for office productivity applications to be invoked with various commands. Each application is given a different named scheme but all schemes follow the same rules for how the URI is formed (URI Schema).</span></span>
  
## <a name="13-uri-schema"></a><span data-ttu-id="ea8cf-110">1.3 URI-SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ea8cf-110">1.3 URI SCHEMA</span></span>

### <a name="full-schema"></a><span data-ttu-id="ea8cf-111">Vollständiges Schema</span><span class="sxs-lookup"><span data-stu-id="ea8cf-111">Full schema</span></span>

<span data-ttu-id="ea8cf-112">< *Schemaname*  >:<  *Befehlsname*  >„|"<  *Befehlsargumentdeskriptor*  >„|"<  *Befehlsargument*  ></span><span class="sxs-lookup"><span data-stu-id="ea8cf-112">< *scheme-name*  >:<  *command-name*  >"|"<  *command-argument-descriptor*  > "|"<  *command-argument*  ></span></span> 
  
<span data-ttu-id="ea8cf-p103">Ein der Definition in diesem Dokument entsprechender URI kann ein oder mehrere Befehlsargumente aufweisen, die die Elemente < *Befehlsargumentdeskriptor*  > und <  *Befehlsargument*  > enthalten und durch den senkrechten Strich („|") getrennt sind. Wenn mehrere Befehlsargumente in einem URI enthalten sind, muss jedes Befehlsargument durch einen senkrechten Strich („|") vom nächsten Befehlsargument getrennt sein.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p103">A URI as defined in this document may have one or more command arguments, each of which must include both the < *command-argument-descriptor*  > and the <  *command-argument*  > elements and be delimited by the vertical bar ("|") character. When more than one command argument is included in a URI there must be a vertical bar ("|") character separating each command argument from the following command argument.</span></span> 
  
<span data-ttu-id="ea8cf-p104">Diese Schemas enthalten keine Autoritätskomponente, wie in RFC 3986, Abschnitt 3.2 definiert. Der Aufruf der in diesem Dokument angegebenen Befehle erfolgt im Kontext des Systems, das den Befehl aufruft. Wenn z. B. der URI „ms-excel:ofv|u|http://contoso/Q4/budget.xls" von einem Personalcomputer unter Microsoft Windows mit Microsoft Office 2013 aufgerufen wird, wird als Ergebnis erwartet, dass die lokale Installation von Microsoft Excel gestartet wird und Argumente zum Öffnen der Datei unter  *http://contoso/Q4/budget.xls*  im schreibgeschützten Modus an sie übergeben werden. Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p104">These schemes do not include an authority component as defined in section 3.2 of RFC 3986. Invocation of the commands specified in this document takes place in the context of the system invoking the command. For example, when the URI "ms-excel:ofv|u|http://contoso/Q4/budget.xls" is invoked from a personal computer running Microsoft Windows with Microsoft Office 2013 installed the expected result is that the local installation of Microsoft Excel will be launched and passed arguments to open the file at  *http://contoso/Q4/budget.xls*  in read-only mode. Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span> 
  
<span data-ttu-id="ea8cf-120">Die Schemasyntax enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ea8cf-120">The scheme syntax includes the following:</span></span>
  
1. <span data-ttu-id="ea8cf-p105">< *Schemaname*  >: Dies bezieht sich auf den Anwendungstyp, der aufgerufen werden soll. Beispielsweise ist der Schemaname „ms-word:" von Microsoft Word registriert.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p105">< *scheme-name*  >: This refers to the type of application that should be invoked. For instance, the ms-word: scheme name is registered by Microsoft Word.</span></span> 
    
2. <span data-ttu-id="ea8cf-123">Trennzeichen „:"</span><span class="sxs-lookup"><span data-stu-id="ea8cf-123">":" separator</span></span>
    
3. <span data-ttu-id="ea8cf-p106">< *Befehlsname*  >: Dies beschreibt die Aktionen, die die Anwendung ausführen soll. Beispielsweise Öffnen eines Dokuments zur Anzeige. Die Liste der Befehlsnamen wird in Abschnitt 1.5 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p106">< *command-name*  >: This describes the actions that the application should perform. For instance, opening a document for viewing. The list of command names is described in section 1.5.</span></span> 
    
4. <span data-ttu-id="ea8cf-127">Trennzeichen „|" (senkrechter Strich)</span><span class="sxs-lookup"><span data-stu-id="ea8cf-127">"|" (vertical bar) separator</span></span>
    
5. <span data-ttu-id="ea8cf-128">< *Befehlsargumentdeskriptor*  >: Dieses Element enthält weitere Informationen zur Bedeutung des Befehlsarguments.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-128">< *command-argument-descriptor*  >: This element gives more information about what the command argument is about.</span></span> 
    
6. <span data-ttu-id="ea8cf-129">Trennzeichen „|" (senkrechter Strich)</span><span class="sxs-lookup"><span data-stu-id="ea8cf-129">"|" (vertical bar) separator</span></span>
    
7. <span data-ttu-id="ea8cf-p107">< *Befehlsargument*  >: Die Argumente variieren je nach Befehl. Ein allgemeines Argument ist der URI eines Dokuments, in der Regel nach dem HTTP- oder HTTPS-Schema. Beachten Sie, dass in <  *Befehlsargument*  >-Segmenten die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen sind und daher ohne Escapezeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p107">< *command-argument*  >: The arguments vary depending on the command. One common argument is the URI to a document, typically using the http or https scheme. Note that within <  *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
    
### <a name="abbreviated-schema"></a><span data-ttu-id="ea8cf-133">Verkürztes Schema</span><span class="sxs-lookup"><span data-stu-id="ea8cf-133">Abbreviated schema</span></span>

<span data-ttu-id="ea8cf-p108">Eine Kurzform des Office-URI-Schemas ermöglicht eine kompaktere Anforderung, um eine angegebene Office-Anwendung zu starten und die Ressource unter einem angegebenen URI zu öffnen. Diese Kurzform umfasst den < *Befehlsnamen*  > „ofv" und den <  *Befehlsargumentdeskriptor*  > „u". In diesem Schema sind keine weiteren Befehle oder Argumente zulässig.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p108">An abbreviated form of the office URI schemes allows for a more compact request to launch a specified Office application to open the resource located at a given URI. This abbreviated form implies the < *command-name*  > "ofv" and the <  *command-argument-descriptor*  > "u". No further commands or command arguments are allowed in this schema.</span></span> 
  
<span data-ttu-id="ea8cf-137">< *Schemaname*  >:<  *Befehlsargument*  ></span><span class="sxs-lookup"><span data-stu-id="ea8cf-137">< *scheme-name*  >:<  *command-argument*  ></span></span> 
  
1. <span data-ttu-id="ea8cf-p109">< *Schemaname*  >: Der Anwendungstyp, der aufgerufen werden soll. Zum Beispiel „ms-word:" für Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p109">< *scheme-name*  >: the type of application that should be invoked. For instance ms-word: for Microsoft Word.</span></span> 
    
2. <span data-ttu-id="ea8cf-p110">< *Befehlsargument*  >: Der URI für die Ressource, die die Anwendung öffnen soll. Derzeit werden nur URIs auf Grundlage des HTTP- oder HTTPS-Schemas unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p110">< *command-argument*  >: URI for the resource the application should open. Currently only URIs based on the http or https scheme are supported.</span></span> 
    
## <a name="14-scheme-names-and-office-application-registrations"></a><span data-ttu-id="ea8cf-142">1.4 SCHEMANAMEN UND OFFICE-ANWENDUNGSREGISTRIERUNGEN</span><span class="sxs-lookup"><span data-stu-id="ea8cf-142">1.4 SCHEME NAMES AND OFFICE APPLICATION REGISTRATIONS</span></span>

<span data-ttu-id="ea8cf-p111">Im Folgenden finden Sie die Liste der in Microsoft Office-Anwendungen implementierten Schemanamen. Bei der Installation von Microsoft Office wird jeder Schemaname in Windows registriert, damit er vom Office-Produkt desselben Namens verarbeitet werden kann. Beachten Sie, dass „ms-spd" eine Abkürzung für SharePoint Designer ist.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p111">The following is the list of scheme names implemented in Microsoft Office applications. When Microsoft Office is installed, each scheme name is registered with Windows to be handled by the Office product of the same name. Note that "ms-spd" is an abbreviation for SharePoint Designer.</span></span>
  
> - <span data-ttu-id="ea8cf-146">*ms-word:*</span><span class="sxs-lookup"><span data-stu-id="ea8cf-146">*ms-word:*</span></span> 
    
> - <span data-ttu-id="ea8cf-147">*ms-powerpoint:*</span><span class="sxs-lookup"><span data-stu-id="ea8cf-147">*ms-powerpoint:*</span></span> 
    
> - <span data-ttu-id="ea8cf-148">*ms-excel:*</span><span class="sxs-lookup"><span data-stu-id="ea8cf-148">*ms-excel:*</span></span> 
    
> - <span data-ttu-id="ea8cf-149">*ms-visio:*</span><span class="sxs-lookup"><span data-stu-id="ea8cf-149">*ms-visio:*</span></span> 
    
> - <span data-ttu-id="ea8cf-150">*ms-access:*</span><span class="sxs-lookup"><span data-stu-id="ea8cf-150">*ms-access:*</span></span> 
    
> - <span data-ttu-id="ea8cf-151">*ms-project:*</span><span class="sxs-lookup"><span data-stu-id="ea8cf-151">*ms-project:*</span></span> 
    
> - <span data-ttu-id="ea8cf-152">*ms-publisher:*</span><span class="sxs-lookup"><span data-stu-id="ea8cf-152">*ms-publisher:*</span></span> 
    
> - <span data-ttu-id="ea8cf-153">*ms-spd:*</span><span class="sxs-lookup"><span data-stu-id="ea8cf-153">*ms-spd:*</span></span> 
    
> - <span data-ttu-id="ea8cf-154">*ms-infopath:*</span><span class="sxs-lookup"><span data-stu-id="ea8cf-154">*ms-infopath:*</span></span> 
    
## <a name="15-commands-and-required-command-arguments"></a><span data-ttu-id="ea8cf-155">1.5 BEFEHLE UND ERFORDERLICHE BEFEHLSARGUMENTE</span><span class="sxs-lookup"><span data-stu-id="ea8cf-155">1.5 COMMANDS AND REQUIRED COMMAND ARGUMENTS</span></span>

### <a name="view-document"></a><span data-ttu-id="ea8cf-156">Dokument anzeigen</span><span class="sxs-lookup"><span data-stu-id="ea8cf-156">View Document</span></span>

<span data-ttu-id="ea8cf-157">Der folgende Befehl bewirkt das Öffnen des vom URI referenzierten Dokuments in der Anwendung im schreibgeschützten Modus oder im Anzeigemodus.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-157">The following command will cause the application to open the document referenced by the URI in a read-only or view mode.</span></span>
  
> <span data-ttu-id="ea8cf-158">Befehlsname: ofv</span><span class="sxs-lookup"><span data-stu-id="ea8cf-158">Command Name: ofv</span></span>
    
> <span data-ttu-id="ea8cf-159">Befehlsargumentdeskriptor: u</span><span class="sxs-lookup"><span data-stu-id="ea8cf-159">Command argument descriptor: u</span></span>
    
> <span data-ttu-id="ea8cf-160">Befehlsargument: ein URI zum Dokument auf Basis des HTTP- oder HTTPS-Schemas</span><span class="sxs-lookup"><span data-stu-id="ea8cf-160">Command argument: a URI to the document, based on the http or https scheme</span></span>
    
> <span data-ttu-id="ea8cf-161">Beispiel:  *ms-excel:ofv|u|http://contoso/Q4/budget.xls*</span><span class="sxs-lookup"><span data-stu-id="ea8cf-161">Example:  *ms-excel:ofv|u|http://contoso/Q4/budget.xls*</span></span> 
    
### <a name="edit-document"></a><span data-ttu-id="ea8cf-162">Dokument bearbeiten</span><span class="sxs-lookup"><span data-stu-id="ea8cf-162">Edit Document</span></span>

<span data-ttu-id="ea8cf-163">Der folgende Befehl bewirkt das Öffnen des vom URI referenzierten Dokuments in der Anwendung im Bearbeitungsmodus.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-163">The following command will cause the application to open the document referenced by the URI in editing mode.</span></span>
  
> <span data-ttu-id="ea8cf-164">Befehlsname: ofe</span><span class="sxs-lookup"><span data-stu-id="ea8cf-164">Command Name: ofe</span></span>
    
> <span data-ttu-id="ea8cf-165">Befehlsargumentdeskriptor: u</span><span class="sxs-lookup"><span data-stu-id="ea8cf-165">Command argument descriptor: u</span></span>
    
> <span data-ttu-id="ea8cf-166">Befehlsargument: ein URI zum Dokument auf Basis des HTTP- oder HTTPS-Schemas</span><span class="sxs-lookup"><span data-stu-id="ea8cf-166">Command argument: a URI to the document, based on the http or https scheme</span></span>
    
> <span data-ttu-id="ea8cf-167">Beispiel:  *ms-powerpoint:ofe|u|http://www.fourthcoffee.com/AllHandsDeck.ppt*</span><span class="sxs-lookup"><span data-stu-id="ea8cf-167">Example:  *ms-powerpoint:ofe|u|http://www.fourthcoffee.com/AllHandsDeck.ppt*</span></span> 
    
### <a name="new-document-from-template"></a><span data-ttu-id="ea8cf-168">Neues Dokument aus Vorlage</span><span class="sxs-lookup"><span data-stu-id="ea8cf-168">New Document from Template</span></span>

<span data-ttu-id="ea8cf-p112">Der folgende Befehl bewirkt das Erstellen und Öffnen eines neuen Dokuments in der Anwendung, basierend auf der unter dem angegebenen URI gespeicherten Vorlage. Die Vorlagendatei wird dabei nicht geändert. In einem zusätzlichen Befehlsargument kann der Standardpfad angegeben werden, der beim ersten Speichern der Datei als Speicherort angeboten wird. Der Benutzer kann einen anderen Speicherort auswählen.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p112">The following command will cause the application to create and open a new document based on the template stored at the specified URI. The template file is not modified in this process. An additional command argument may be supplied to specify the default path offered as a save location when the file is first saved. It is possible for the user to choose a different location.</span></span>
  
> <span data-ttu-id="ea8cf-173">Befehlsname: nft</span><span class="sxs-lookup"><span data-stu-id="ea8cf-173">Command Name: nft</span></span>
    
> <span data-ttu-id="ea8cf-174">Befehlsargumentdeskriptor 1: u</span><span class="sxs-lookup"><span data-stu-id="ea8cf-174">Command argument descriptor 1: u</span></span>
    
> <span data-ttu-id="ea8cf-175">Befehlsargument: ein URI zur Vorlage auf Basis des HTTP- oder HTTPS-Schemas</span><span class="sxs-lookup"><span data-stu-id="ea8cf-175">Command argument 1: a URI to the template, based on the http or https scheme</span></span>
    
> <span data-ttu-id="ea8cf-176">Optionaler Befehlsargumentdeskriptor 2: s</span><span class="sxs-lookup"><span data-stu-id="ea8cf-176">Optional Command argument descriptor 2: s</span></span>
    
> <span data-ttu-id="ea8cf-177">Optionales Befehlsargument 2: ein URI zur Angabe des Standardspeicherordners</span><span class="sxs-lookup"><span data-stu-id="ea8cf-177">Optional Command argument 2: URI to specify the default save folder</span></span>
    
> <span data-ttu-id="ea8cf-178">Beispiel:  *ms-word:nft|u|http://cohowinery/templates/elegance.pot|s|http://cohowinery/presentations*</span><span class="sxs-lookup"><span data-stu-id="ea8cf-178">Example:  *ms-word:nft|u|http://cohowinery/templates/elegance.pot|s|http://cohowinery/presentations*</span></span> 
    
<span data-ttu-id="ea8cf-179">Hinweis: Wenn der optionale Standardspeicherort angegeben wird, muss er auf denselben Hostnamen verweisen wie die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-179">As a note, if the optional default save location is supplied, it must be pointing to the same host name as the template.</span></span>
  
<span data-ttu-id="ea8cf-180">Außerdem wird die Funktion „Neues Dokument aus Vorlage" von den Anwendungen SharePoint Designer und InfoPath (die das Schema „ms-spd:" bzw. „ms-infopath:" implementieren) nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-180">Additionally, the SharePoint Designer and InfoPath applications (which implement the ms-spd: scheme and ms-infopath: schemes, respectively) do not support the "new document from template" functionality.</span></span>
  
## <a name="16-backwards-compatibility"></a><span data-ttu-id="ea8cf-181">1.6 ABWÄRTSKOMPATIBILITÄT</span><span class="sxs-lookup"><span data-stu-id="ea8cf-181">1.6 BACKWARDS COMPATIBILITY</span></span>

<span data-ttu-id="ea8cf-p113">Bei der Analyse eines URI zum Extrahieren der entsprechenden Befehlsargumente für einen bestimmten Befehl verwendet der Office-URI-Handler nur die Befehlsargumente, die den erwarteten Befehlsargumentdeskriptor aufweisen. Wenn weitere Paare von Argumenten und Argumentdeskriptoren vorhanden sind, die unerwartete Argumentdeskriptoren haben, werden sie aus dem URI entfernt. Dieser Mechanismus ermöglicht es, in zukünftigen Versionen des Schemas zusätzliche Befehlsargumente hinzuzufügen, ohne die Abwärtskompatibilität mit älteren Implementierungen dieses Schemas zu gefährden.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p113">When parsing a URI to extract the appropriate command arguments for a given command, the Office URI handler will only use the command arguments that have the expected command argument descriptor. If there are additional pairs of arguments and argument descriptors that have unexpected argument descriptors, they will be removed from the URI. This mechanism allows future versions of the scheme to add additional command arguments without breaking backward compatibility with legacy implementations of this scheme.</span></span>
  
## <a name="17-implementation-restrictions-on-command-arguments"></a><span data-ttu-id="ea8cf-185">1.7 IMPLEMENTIERUNGSEINSCHRÄNKUNGEN FÜR BEFEHLSARGUMENTE</span><span class="sxs-lookup"><span data-stu-id="ea8cf-185">1.7 IMPLEMENTATION RESTRICTIONS ON COMMAND ARGUMENTS</span></span>

<span data-ttu-id="ea8cf-186">Die folgenden Einschränkungen gelten für Befehlsargumente in der aktuellen Implementierung in Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-186">The below restrictions are placed on command arguments in its current implementation in Office 2013.</span></span>
  
### <a name="length-limitations-on-uri-command-arguments"></a><span data-ttu-id="ea8cf-187">Längenbeschränkungen für URI-Befehlsargumente</span><span class="sxs-lookup"><span data-stu-id="ea8cf-187">Length limitations on URI command arguments</span></span>

<span data-ttu-id="ea8cf-p114">Die maximale Länge für URI-Befehlsargumente beträgt 256 Zeichen für alle Apps mit Ausnahme von Excel; hier beträgt der Grenzwert 216. Längere Pfade werden möglicherweise von einzelnen Apps unterstützt. Es wird empfohlen, dies vor der Bereitstellung von Lösungen zu testen, die längere Pfade verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p114">For URI command arguments, the maximum path length is 256 characters for all apps except Excel, where the limit is 216. Path lengths greater than these may be supported on an app-by-app basis and testing is recommended before deploying any solutions that rely on this.</span></span>
  
### <a name="allowed-characters-in-uri-command-arguments"></a><span data-ttu-id="ea8cf-190">Zulässige Zeichen in URI-Befehlsargumenten</span><span class="sxs-lookup"><span data-stu-id="ea8cf-190">Allowed characters in URI command arguments</span></span>

<span data-ttu-id="ea8cf-p115">Zulässige URIs müssen den in RFC 3987 - Internationalized Resource Identifiers (IRIs) - vorgeschlagenen Standards entsprechen. In RFC 3986 als reserviert aufgeführte Zeichen dürfen nicht mit Prozentzeichen codiert werden. Dateinamen dürfen die folgenden Zeichen nicht enthalten: \ / : ? \< \> | " oder \*.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p115">Allowed URIs must conform to the standards proposed in RFC 3987 - Internationalized Resource Identifiers (IRIs) . Characters identified as reserved in RFC 3986 should not be percent encoded. . Filenames must not contain any of the following characters: \ / : ? \< \> | " or \*.</span></span>  
  
## <a name="appendix-a---uri-scheme-registration-template-for-ms-word-scheme"></a><span data-ttu-id="ea8cf-196">ANHANG A - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-WORD-SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ea8cf-196">APPENDIX A - URI SCHEME REGISTRATION TEMPLATE FOR MS-WORD SCHEME</span></span>
<span data-ttu-id="ea8cf-197"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="ea8cf-197"></span></span>

### <a name="a-3-uri-scheme-syntax"></a><span data-ttu-id="ea8cf-p116">A-3. URI-Schemasyntax</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p116">A-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="ea8cf-200">Word-Schema = „ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="ea8cf-200">Word Scheme = "ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="ea8cf-201">open-for-edit-cmd = „ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-201">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="ea8cf-202">open-for-view-cmd = „ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-202">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="ea8cf-203">new-from-template-cmd = „nft|u|" template-uri [„|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="ea8cf-203">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="ea8cf-204">document-uri = URI-Speicherort des zu öffnenden Dokuments</span><span class="sxs-lookup"><span data-stu-id="ea8cf-204">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="ea8cf-205">template-uri = URI-Speicherort der Vorlagendatei, auf der die neue Datei basiert</span><span class="sxs-lookup"><span data-stu-id="ea8cf-205">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="ea8cf-206">save-location = URI-Speicherort des Ordners, in dem das neue Dokument erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="ea8cf-206">save-location = URI location of folder in which new document should be created</span></span>
    
### <a name="a-4-uri-scheme-semantics"></a><span data-ttu-id="ea8cf-p117">A-4. URI-Schemasemantik</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p117">A-4. URI Scheme Semantics</span></span>

<span data-ttu-id="ea8cf-p118">Das Schema „ms-word" definiert eine URI-Syntax zum Öffnen oder Erstellen eines Textverarbeitungsdokuments. Das Schema definiert drei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der eine Textverarbeitungsanwendung anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, (2) open-for-view-cmd (ofv), der eine Textverarbeitungsanwendung anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen, und 3) new-from-template-cmd (nft), der eine Textverarbeitungsanwendung anweist, ein neues Dokument basierend auf der Dokumentvorlage am angegebenen URI „template-uri" zu erstellen und entweder am im optionalen URI „save-location" angegebenen Speicherort oder, bei Nichtvorhandensein dieses optionalen URI, in der Standarddokumentbibliothek zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p118">The ms-word scheme defines a URI syntax for opening or creating a word processing document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a word processing application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a word processing application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a word processing application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="a-5-applicationsprotocols-that-use-the-ms-word-uri-scheme"></a><span data-ttu-id="ea8cf-p119">A-5. Anwendungen/Protokolle, die das URI-Schema „ms-word" verwenden</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p119">A-5. Applications/Protocols that use the ms-word URI Scheme</span></span>

<span data-ttu-id="ea8cf-p120">Das URI-Schema „ms-word" wird von Microsoft Office 2013 zum Aufrufen von Microsoft Word 2013 oder Microsoft Word 2010 mit Service Pack 2 verwendet. Microsoft SharePoint 2013 verwendet ms-word-URIs als Links zu Textverarbeitungsdokumenten in SharePoint-Dokumentbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p120">The ms-word URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Word 2013 or Microsoft Word 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-word URIs as links to word processing documents stored in SharePoint document libraries.</span></span>
  
### <a name="a-6-interoperability-considerations"></a><span data-ttu-id="ea8cf-p121">A-6. Überlegungen zur Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p121">A-6. Interoperability Considerations</span></span>

<span data-ttu-id="ea8cf-p122">Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p122">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters.. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="ea8cf-220">In < *Befehlsargument*  >-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-220">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="a-7-security-considerations"></a><span data-ttu-id="ea8cf-p123">A-7. Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p123">A-7. Security Considerations</span></span>

 <span data-ttu-id="ea8cf-p124">Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-word-URIs bewirkt das Klicken auf einen Link zu einem ms-word-URI den Start der registrierten Textverarbeitungsanwendung. Dabei werden an die Textverarbeitungsanwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Textverarbeitungsanwendungen, die zur Verarbeitung von ms-word-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p124">On systems that have registered handlers to recognize and act on ms-word URIs, clicking on a link to an ms-word URI will cause the registered word processing application to be launched, with instructions to the word processing application to attempt to open a document at the specified URI. Word processing applications registering to process ms-word URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span> 
  
### <a name="a-8-references"></a><span data-ttu-id="ea8cf-p125">A-8. Referenzen</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p125">A-8. References</span></span>

<span data-ttu-id="ea8cf-227">RFC 3987 - International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="ea8cf-227">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-b---uri-scheme-registration-template-for-ms-powerpoint-scheme"></a><span data-ttu-id="ea8cf-228">ANHANG B - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-POWERPOINT-SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ea8cf-228">APPENDIX B - URI SCHEME REGISTRATION TEMPLATE FOR MS-POWERPOINT SCHEME</span></span>
<span data-ttu-id="ea8cf-229"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="ea8cf-229"></span></span>

### <a name="b-3-uri-scheme-syntax"></a><span data-ttu-id="ea8cf-p126">B-3. URI-Schemasyntax</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p126">B-3. URI Scheme Syntax</span></span>

- <span data-ttu-id="ea8cf-232">PowerPoint-Schema = „ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="ea8cf-232">PowerPoint Scheme = "ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
- <span data-ttu-id="ea8cf-233">open-for-edit-cmd = „ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-233">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
- <span data-ttu-id="ea8cf-234">open-for-view-cmd = „ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-234">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
- <span data-ttu-id="ea8cf-235">new-from-template-cmd = „nft|u|" template-uri [„|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="ea8cf-235">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
- <span data-ttu-id="ea8cf-236">document-uri = URI-Speicherort des zu öffnenden Dokuments</span><span class="sxs-lookup"><span data-stu-id="ea8cf-236">document-uri = URI location of document to open</span></span>
    
- <span data-ttu-id="ea8cf-237">template-uri = URI-Speicherort der Vorlagendatei, auf der die neue Datei basiert</span><span class="sxs-lookup"><span data-stu-id="ea8cf-237">template-uri = URI location of template file upon which new file will be based</span></span>
    
- <span data-ttu-id="ea8cf-238">save-location\* = URI-Speicherort des Ordners, in dem das neue Dokument erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="ea8cf-238">save-location\* = URI location of folder in which new document should be created</span></span>
    
- <span data-ttu-id="ea8cf-239">\*save-location ist ein optionaler Parameter</span><span class="sxs-lookup"><span data-stu-id="ea8cf-239">\*save-location is an optional parameter</span></span>
    
### <a name="b-4-uri-scheme-semantics"></a><span data-ttu-id="ea8cf-p127">B-4. URI-Schemasemantik</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p127">B-4. URI Scheme Semantics</span></span>

<span data-ttu-id="ea8cf-p128">Das Schema „ms-powerpoint" definiert eine URI-Syntax zum Öffnen oder Erstellen eines Präsentationsdokuments. Das Schema definiert drei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der eine Präsentationsanwendung anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, (2) open-for-view-cmd (ofv), der eine Präsentationsanwendung anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen, und 3) new-from-template-cmd (nft), der eine Präsentationsanwendung anweist, ein neues Dokument basierend auf der Dokumentvorlage am angegebenen URI „template-uri" zu erstellen und entweder am im optionalen URI „save-location" angegebenen Speicherort oder, bei Nichtvorhandensein dieses optionalen URI, in der Standarddokumentbibliothek zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p128">The ms-powerpoint scheme defines a URI syntax for opening or creating a presentation document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a presentation application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a presentation application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a presentation application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="b-5-applicationsprotocols-that-use-the-ms-powerpoint-uri-scheme"></a><span data-ttu-id="ea8cf-p129">B-5. Anwendungen/Protokolle, die das URI-Schema „ms-powerpoint" verwenden</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p129">B-5. Applications/Protocols that use the ms-powerpoint URI Scheme</span></span>

<span data-ttu-id="ea8cf-p130">Das URI-Schema „ms-powerpoint" wird von Microsoft Office 2013 zum Aufrufen von Microsoft PowerPoint 2013 oder Microsoft PowerPoint 2010 mit Service Pack 2 verwendet. Microsoft SharePoint 2013 verwendet ms-powerpoint-URIs als Links zu Präsentationsdokumenten in SharePoint-Dokumentbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p130">The ms-powerpoint URI Scheme is used by Microsoft Office 2013 to invoke Microsoft PowerPoint 2013 or Microsoft PowerPoint 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-powerpoint URIs as links to presentation documents stored in SharePoint document libraries.</span></span>
  
### <a name="b-6-interoperability-considerations"></a><span data-ttu-id="ea8cf-p131">B-6. Überlegungen zur Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p131">B-6. Interoperability Considerations</span></span>

<span data-ttu-id="ea8cf-p132">Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p132">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="ea8cf-253">In < *Befehlsargument*  >-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-253">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="b-7-security-considerations"></a><span data-ttu-id="ea8cf-p133">B-7. Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p133">B-7. Security Considerations</span></span>

<span data-ttu-id="ea8cf-p134">Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-powerpoint-URIs bewirkt das Klicken auf einen Link zu einem ms-powerpoint-URI den Start der registrierten Präsentationsanwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-powerpoint-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p134">On systems that have registered handlers to recognize and act on ms-powerpoint URIs, clicking on a link to an ms-powerpoint URI will cause the registered presentation application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-powerpoint URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="b-8-references"></a><span data-ttu-id="ea8cf-p135">B-8. Referenzen</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p135">B-8. References</span></span>

<span data-ttu-id="ea8cf-260">RFC 3987 - International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="ea8cf-260">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-c---uri-scheme-registration-template-for-ms-excel-scheme"></a><span data-ttu-id="ea8cf-261">ANHANG C - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-EXCEL-SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ea8cf-261">APPENDIX C - URI SCHEME REGISTRATION TEMPLATE FOR MS-EXCEL SCHEME</span></span>
<span data-ttu-id="ea8cf-262"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="ea8cf-262"></span></span>

### <a name="c-3-uri-scheme-syntax"></a><span data-ttu-id="ea8cf-p136">C-3. URI-Schemasyntax</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p136">C-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="ea8cf-265">Excel-Schema = „ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="ea8cf-265">Excel Scheme = "ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="ea8cf-266">open-for-edit-cmd = „ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-266">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="ea8cf-267">open-for-view-cmd = „ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-267">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="ea8cf-268">new-from-template-cmd = „nft|u|" template-uri [„|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="ea8cf-268">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="ea8cf-269">document-uri = URI-Speicherort des zu öffnenden Dokuments</span><span class="sxs-lookup"><span data-stu-id="ea8cf-269">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="ea8cf-270">template-uri = URI-Speicherort der Vorlagendatei, auf der die neue Datei basiert</span><span class="sxs-lookup"><span data-stu-id="ea8cf-270">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="ea8cf-271">save-location\* = URI-Speicherort des Ordners, in dem das neue Dokument erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="ea8cf-271">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="ea8cf-272">\*save-location ist ein optionaler Parameter</span><span class="sxs-lookup"><span data-stu-id="ea8cf-272">\*save-location is an optional parameter</span></span>
    
### <a name="c-4-uri-scheme-semantics"></a><span data-ttu-id="ea8cf-p137">C-4. URI-Schemasemantik</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p137">C-4. URI Scheme Semantics</span></span>

<span data-ttu-id="ea8cf-p138">Das Schema „ms-excel" definiert eine URI-Syntax zum Öffnen oder Erstellen eines Tabellenblatts. Das Schema definiert drei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der eine Tabellenkalkulationsanwendung anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, (2) open-for-view-cmd (ofv), der eine Tabellenkalkulationsanwendung anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen, und 3) new-from-template-cmd (nft), der eine Tabellenkalkulationsanwendung anweist, ein neues Dokument basierend auf der Dokumentvorlage am angegebenen URI „template-uri" zu erstellen und entweder am im optionalen URI „save-location" angegebenen Speicherort oder, bei Nichtvorhandensein dieses optionalen URI, in der Standarddokumentbibliothek zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p138">The ms-excel scheme defines a URI syntax for opening or creating a spreadsheet document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a spreadsheet application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a spreadsheet application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a spreadsheet application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="c-5-applicationsprotocols-that-use-the-ms-excel-uri-scheme"></a><span data-ttu-id="ea8cf-p139">C-5. Anwendungen/Protokolle, die das URI-Schema „ms-excel" verwenden</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p139">C-5. Applications/Protocols that use the ms-excel URI Scheme</span></span>

<span data-ttu-id="ea8cf-p140">Das URI-Schema „ms-excel" wird von Microsoft Office 2013 zum Aufrufen von Microsoft Excel 2013 oder Microsoft Excel 2010 mit Service Pack 2 verwendet. Microsoft SharePoint 2013 verwendet ms-excel-URIs als Links zu Tabellenblättern in SharePoint-Dokumentbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p140">The ms-excel URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Excel 2013 or Microsoft Excel 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-excel URIs as links to spreadsheet documents stored in SharePoint document libraries.</span></span>
  
### <a name="c-6-interoperability-considerations"></a><span data-ttu-id="ea8cf-p141">C-6. Überlegungen zur Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p141">C-6. Interoperability Considerations</span></span>

<span data-ttu-id="ea8cf-p142">Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p142">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="ea8cf-286">In < *Befehlsargument*  >-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-286">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="c-7-security-considerations"></a><span data-ttu-id="ea8cf-p143">C-7. Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p143">C-7. Security Considerations</span></span>

<span data-ttu-id="ea8cf-p144">Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-excel-URIs bewirkt das Klicken auf einen Link zu einem ms-excel-URI den Start der registrierten Tabellenkalkulationsanwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-excel-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p144">On systems that have registered handlers to recognize and act on ms-excel URIs, clicking on a link to an ms-excel URI will cause the registered spreadsheet application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-excel URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="c-8-references"></a><span data-ttu-id="ea8cf-p145">C-8. Referenzen</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p145">C-8. References</span></span>

<span data-ttu-id="ea8cf-293">RFC 3987 - International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="ea8cf-293">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-d---uri-scheme-registration-template-for-ms-visio-scheme"></a><span data-ttu-id="ea8cf-294">ANHANG D - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-VISIO-SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ea8cf-294">APPENDIX D - URI SCHEME REGISTRATION TEMPLATE FOR MS-VISIO SCHEME</span></span>
<span data-ttu-id="ea8cf-295"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="ea8cf-295"></span></span>

### <a name="d-3-uri-scheme-syntax"></a><span data-ttu-id="ea8cf-p146">D-3. URI-Schemasyntax</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p146">D-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="ea8cf-298">Visio-Schema = „ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="ea8cf-298">Visio Scheme = "ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="ea8cf-299">open-for-edit-cmd = „ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-299">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="ea8cf-300">open-for-view-cmd = „ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-300">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="ea8cf-301">new-from-template-cmd = „nft|u|" template-uri [„|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="ea8cf-301">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="ea8cf-302">document-uri = URI-Speicherort des zu öffnenden Dokuments</span><span class="sxs-lookup"><span data-stu-id="ea8cf-302">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="ea8cf-303">template-uri = URI-Speicherort der Vorlagendatei, auf der die neue Datei basiert</span><span class="sxs-lookup"><span data-stu-id="ea8cf-303">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="ea8cf-304">save-location\* = URI-Speicherort des Ordners, in dem das neue Dokument erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="ea8cf-304">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="ea8cf-305">\*save-location ist ein optionaler Parameter</span><span class="sxs-lookup"><span data-stu-id="ea8cf-305">\*save-location is an optional parameter</span></span>
    
### <a name="d-4-uri-scheme-semantics"></a><span data-ttu-id="ea8cf-p147">D-4. URI-Schemasemantik</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p147">D-4. URI Scheme Semantics</span></span>

<span data-ttu-id="ea8cf-p148">Das Schema „ms-visio" definiert eine URI-Syntax zum Öffnen oder Erstellen eines Microsoft Visio-Dokuments. Das Schema definiert drei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der Visio anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, (2) open-for-view-cmd (ofv), der Visio anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen, und 3) new-from-template-cmd (nft), der Visio anweist, ein neues Dokument basierend auf der Dokumentvorlage am angegebenen URI „template-uri" zu erstellen und entweder am im optionalen URI „save-location" angegebenen Speicherort oder, bei Nichtvorhandensein dieses optionalen URI, in der Standarddokumentbibliothek zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p148">The ms-visio scheme defines a URI syntax for opening or creating a Microsoft Visio document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Visio to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Visio to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Visio to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="d-5-applicationsprotocols-that-use-the-ms-visio-uri-scheme"></a><span data-ttu-id="ea8cf-p149">D-5. Anwendungen/Protokolle, die das URI-Schema „ms-visio" verwenden</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p149">D-5. Applications/Protocols that use the ms-visio URI Scheme</span></span>

<span data-ttu-id="ea8cf-p150">Das URI-Schema „ms-visio" wird von Microsoft Office 2013 zum Aufrufen von Microsoft Visio 2013 oder Microsoft Visio 2010 mit Service Pack 2 verwendet. Microsoft SharePoint 2013 verwendet ms-visio-URIs als Links zu Visio-Dokumenten in SharePoint-Dokumentbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p150">The ms-visio URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Visio 2013 or Microsoft Visio 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-visio URIs as links to Visio documents stored in SharePoint document libraries.</span></span>
  
### <a name="d-6-interoperability-considerations"></a><span data-ttu-id="ea8cf-p151">D-6. Überlegungen zur Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p151">D-6. Interoperability Considerations</span></span>

<span data-ttu-id="ea8cf-p152">Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p152">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="ea8cf-319">In < *Befehlsargument*  >-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-319">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="d-7-security-considerations"></a><span data-ttu-id="ea8cf-p153">D-7. Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p153">D-7. Security Considerations</span></span>

<span data-ttu-id="ea8cf-p154">Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-visio-URIs bewirkt das Klicken auf einen Link zu einem ms-visio-URI den Start der registrierten Anwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-visio-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p154">On systems that have registered handlers to recognize and act on ms-visio URIs, clicking on a link to an ms-visio URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-visio URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="d-8-references"></a><span data-ttu-id="ea8cf-p155">D-8. Referenzen</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p155">D-8. References</span></span>

<span data-ttu-id="ea8cf-326">RFC 3987 - International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="ea8cf-326">RFC 3987 - International Resource Identifiers (IRIs)</span></span>
  
## <a name="appendix-e---uri-scheme-registration-template-for-ms-access-scheme"></a><span data-ttu-id="ea8cf-327">ANHANG E - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-ACCESS-SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ea8cf-327">APPENDIX E - URI SCHEME REGISTRATION TEMPLATE FOR MS-ACCESS SCHEME</span></span>
<span data-ttu-id="ea8cf-328"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="ea8cf-328"></span></span>

### <a name="e-3-uri-scheme-syntax"></a><span data-ttu-id="ea8cf-p156">E-3. URI-Schemasyntax</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p156">E-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="ea8cf-331">Access-Schema = „ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="ea8cf-331">Access Scheme = "ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="ea8cf-332">open-for-edit-cmd = „ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-332">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="ea8cf-333">open-for-view-cmd = „ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-333">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="ea8cf-334">new-from-template-cmd = „nft|u|" template-uri [„|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="ea8cf-334">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="ea8cf-335">document-uri = URI-Speicherort des zu öffnenden Dokuments</span><span class="sxs-lookup"><span data-stu-id="ea8cf-335">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="ea8cf-336">template-uri = URI-Speicherort der Vorlagendatei, auf der die neue Datei basiert</span><span class="sxs-lookup"><span data-stu-id="ea8cf-336">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="ea8cf-337">save-location\* = URI-Speicherort des Ordners, in dem das neue Dokument erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="ea8cf-337">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="ea8cf-338">\*save-location ist ein optionaler Parameter</span><span class="sxs-lookup"><span data-stu-id="ea8cf-338">\*save-location is an optional parameter</span></span>
    
### <a name="e-4-uri-scheme-semantics"></a><span data-ttu-id="ea8cf-p157">E-4. URI-Schemasemantik</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p157">E-4. URI Scheme Semantics</span></span>

<span data-ttu-id="ea8cf-p158">Das Schema „ms-access" definiert eine URI-Syntax zum Öffnen oder Erstellen einer Datenbank. Das Schema definiert drei Befehle, die als Anweisungen dafür dienen, was mit der referenzierten Datenbankdatei geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der eine Datenbankanwendung anweist, die Datenbank am angegebenen URI für die Bearbeitung zu öffnen, (2) open-for-view-cmd (ofv), der eine Datenbankanwendung anweist, die Datenbank am angegebenen URI im schreibgeschützten Modus zu öffnen, und 3) new-from-template-cmd (nft), der eine Datenbankanwendung anweist, eine neue Datenbank basierend auf der Vorlage am angegebenen URI „template-uri" zu erstellen und entweder am im optionalen URI „save-location" angegebenen Speicherort oder, bei Nichtvorhandensein dieses optionalen URI, in der Standarddokumentbibliothek zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p158">The ms-access scheme defines a URI syntax for opening or creating a database. The scheme defines three commands that serve as instructions regarding what should be done with the referenced database file. The commands are 1) open-for-edit-cmd (ofe), which instructs the database application to open the database at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs the database application to open the database at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs the database application to create a new database based on the template located at the specified template-uri URI and save the new database either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="e-5-applicationsprotocols-that-use-the-ms-access-uri-scheme"></a><span data-ttu-id="ea8cf-p159">E-5. Anwendungen/Protokolle, die das URI-Schema „ms-access" verwenden</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p159">E-5. Applications/Protocols that use the ms-access URI Scheme</span></span>

<span data-ttu-id="ea8cf-p160">Das URI-Schema „ms-access" wird von Microsoft Office 2013 zum Aufrufen von Microsoft Access 2013 oder Microsoft Access 2010 mit Service Pack 2 von Webseiten aus verwendet. Microsoft SharePoint 2013 verwendet ms-access-URIs als Links zu Access-Datenbanken in SharePoint-Dokumentbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p160">The ms-access URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Access 2013 or Microsoft Access 2010 with Service Pack 2 from web pages. Microsoft SharePoint 2013 uses ms-access URIs as links to Access databases stored in SharePoint document libraries.</span></span>
  
### <a name="e-6-interoperability-considerations"></a><span data-ttu-id="ea8cf-p161">E-6. Überlegungen zur Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p161">E-6. Interoperability Considerations</span></span>

<span data-ttu-id="ea8cf-p162">Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können. In \<Befehlsargument\>-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p162">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. Within \<command-argument\> segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span>
  
### <a name="e-7-security-considerations"></a><span data-ttu-id="ea8cf-p163">E-7. Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p163">E-7. Security Considerations</span></span>

<span data-ttu-id="ea8cf-p164">Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-access-URIs bewirkt das Klicken auf einen Link zu einem ms-access-URI den Start der registrierten Anwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen einer Datenbank am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-access-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Datenbanken von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p164">On systems that have registered handlers to recognize and act on ms-access URIs, clicking on a link to an ms-access URI will cause the registered application to be launched, with instructions to the application to attempt to open a database at the specified URI. Applications registering to process ms-access URIs should implement protections to guard against opening databases from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="e-8-references"></a><span data-ttu-id="ea8cf-p165">E-8. Referenzen</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p165">E-8. References</span></span>

<span data-ttu-id="ea8cf-359">RFC 3987 - International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="ea8cf-359">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-f---uri-scheme-registration-template-for-ms-project-scheme"></a><span data-ttu-id="ea8cf-360">ANHANG F - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-PROJECT-SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ea8cf-360">APPENDIX F - URI SCHEME REGISTRATION TEMPLATE FOR MS-PROJECT SCHEME</span></span>
<span data-ttu-id="ea8cf-361"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="ea8cf-361"></span></span>

### <a name="f-3-uri-scheme-syntax"></a><span data-ttu-id="ea8cf-p166">F-3. URI-Schemasyntax</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p166">F-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="ea8cf-364">Project-Schema = „ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="ea8cf-364">Project Scheme = "ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="ea8cf-365">open-for-edit-cmd = „ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-365">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="ea8cf-366">open-for-view-cmd = „ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-366">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="ea8cf-367">new-from-template-cmd = „nft|u|" template-uri [„|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="ea8cf-367">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="ea8cf-368">document-uri = URI-Speicherort des zu öffnenden Dokuments</span><span class="sxs-lookup"><span data-stu-id="ea8cf-368">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="ea8cf-369">template-uri = URI-Speicherort der Vorlagendatei, auf der die neue Datei basiert</span><span class="sxs-lookup"><span data-stu-id="ea8cf-369">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="ea8cf-370">save-location\* = URI-Speicherort des Ordners, in dem das neue Dokument erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="ea8cf-370">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="ea8cf-371">\*save-location ist ein optionaler Parameter</span><span class="sxs-lookup"><span data-stu-id="ea8cf-371">\*save-location is an optional parameter</span></span>
    
### <a name="f-4-uri-scheme-semantics"></a><span data-ttu-id="ea8cf-p167">F-4. URI-Schemasemantik</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p167">F-4. URI Scheme Semantics</span></span>

<span data-ttu-id="ea8cf-p168">Das Schema „ms-project" definiert eine URI-Syntax zum Öffnen oder Erstellen eines Microsoft Project-Dokuments. Das Schema definiert drei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der Project anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, (2) open-for-view-cmd (ofv), der Project anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen, und 3) new-from-template-cmd (nft), der Project anweist, ein neues Dokument basierend auf der Dokumentvorlage am angegebenen URI „template-uri" zu erstellen und entweder am im optionalen URI „save-location" angegebenen Speicherort oder, bei Nichtvorhandensein dieses optionalen URI, in der Standarddokumentbibliothek zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p168">The ms-project scheme defines a URI syntax for opening or creating a Microsoft Project document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Project to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Project to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Project to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="f-5-applicationsprotocols-that-use-the-ms-project-uri-scheme"></a><span data-ttu-id="ea8cf-p169">F-5. Anwendungen/Protokolle, die das URI-Schema „ms-project" verwenden</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p169">F-5. Applications/Protocols that use the ms-project URI Scheme</span></span>

<span data-ttu-id="ea8cf-p170">Das URI-Schema „ms-project" wird von Microsoft Office 2013 zum Aufrufen von Microsoft Project 2013 von Webseiten aus verwendet. Microsoft SharePoint 2013 verwendet ms-project-URIs als Links zu Project-Dokumenten in SharePoint-Dokumentbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p170">The ms-project URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Project 2013 from web pages. Microsoft SharePoint 2013 uses ms-project URIs as links to Project documents stored in SharePoint document libraries.</span></span>
  
### <a name="f-6-interoperability-considerations"></a><span data-ttu-id="ea8cf-p171">F-6. Überlegungen zur Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p171">F-6. Interoperability Considerations</span></span>

<span data-ttu-id="ea8cf-p172">Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p172">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="ea8cf-385">In < *Befehlsargument*  >-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-385">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="f-7-security-considerations"></a><span data-ttu-id="ea8cf-p173">F-7. Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p173">F-7. Security Considerations</span></span>

<span data-ttu-id="ea8cf-p174">Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-project-URIs bewirkt das Klicken auf einen Link zu einem ms-project-URI den Start der registrierten Anwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-project-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p174">On systems that have registered handlers to recognize and act on ms-project URIs, clicking on a link to an ms-project URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-project URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="f-8-references"></a><span data-ttu-id="ea8cf-p175">F-8. Referenzen</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p175">F-8. References</span></span>

<span data-ttu-id="ea8cf-392">RFC 3987 - International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="ea8cf-392">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-g---uri-scheme-registration-template-for-ms-publisher-scheme"></a><span data-ttu-id="ea8cf-393">ANHANG G - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-PUBLISHER-SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ea8cf-393">APPENDIX G - URI SCHEME REGISTRATION TEMPLATE FOR MS-PUBLISHER SCHEME</span></span>
<span data-ttu-id="ea8cf-394"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="ea8cf-394"></span></span>

### <a name="g-3-uri-scheme"></a><span data-ttu-id="ea8cf-p176">G-3. URI-Schema</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p176">G-3. URI Scheme</span></span>

> <span data-ttu-id="ea8cf-397">Syntax Publisher-Schema = „ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="ea8cf-397">Syntax Publisher Scheme = "ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="ea8cf-398">open-for-edit-cmd = „ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-398">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="ea8cf-399">open-for-view-cmd = „ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-399">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="ea8cf-400">new-from-template-cmd = „nft|u|" template-uri [„|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="ea8cf-400">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="ea8cf-401">document-uri = URI-Speicherort des zu öffnenden Dokuments</span><span class="sxs-lookup"><span data-stu-id="ea8cf-401">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="ea8cf-402">template-uri = URI-Speicherort der Vorlagendatei, auf der die neue Datei basiert</span><span class="sxs-lookup"><span data-stu-id="ea8cf-402">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="ea8cf-403">save-location\* = URI-Speicherort des Ordners, in dem das neue Dokument erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="ea8cf-403">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="ea8cf-404">\*save-location ist ein optionaler Parameter</span><span class="sxs-lookup"><span data-stu-id="ea8cf-404">\*save-location is an optional parameter</span></span>
    
### <a name="g-4-uri-scheme-semantics"></a><span data-ttu-id="ea8cf-p177">G-4. URI-Schemasemantik</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p177">G-4. URI Scheme Semantics</span></span>

<span data-ttu-id="ea8cf-p178">Das Schema „ms-publisher" definiert eine URI-Syntax zum Öffnen oder Erstellen eines Microsoft Publisher-Dokuments. Das Schema definiert drei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der Publisher anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, (2) open-for-view-cmd (ofv), der Publisher anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen, und 3) new-from-template-cmd (nft), der Publisher anweist, ein neues Dokument basierend auf der Dokumentvorlage am angegebenen URI „template-uri" zu erstellen und entweder am im optionalen URI „save-location" angegebenen Speicherort oder, bei Nichtvorhandensein dieses optionalen URI, in der Standarddokumentbibliothek zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p178">The ms-publisher scheme defines a URI syntax for opening or creating a Microsoft Publisher document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Publisher to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Publisher to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Publisher to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="g-5-applicationsprotocols-that-use-the-ms-publisher-uri-scheme"></a><span data-ttu-id="ea8cf-p179">G-5. Anwendungen/Protokolle, die das URI-Schema „ms-publisher" verwenden</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p179">G-5. Applications/Protocols that use the ms-publisher URI Scheme</span></span>

<span data-ttu-id="ea8cf-p180">Das URI-Schema „ms-publisher" wird von Microsoft Office 2013 zum Aufrufen von Microsoft Publisher 2013 oder Microsoft Publisher 2010 mit Service Pack 2 von Webseiten aus verwendet. Microsoft SharePoint 2013 verwendet ms-publisher-URIs als Links zu Publisher-Dokumenten in SharePoint-Dokumentbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p180">The ms-publisher URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Publisher 2013 or Microsoft Publisher 2010 with Service Pack 2 from web pages. Microsoft SharePoint 2013 uses ms-publisher URIs as links to Publisher documents stored in SharePoint document libraries.</span></span>
  
### <a name="g-6-interoperability-considerations"></a><span data-ttu-id="ea8cf-p181">G-6. Überlegungen zur Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p181">G-6. Interoperability Considerations</span></span>

<span data-ttu-id="ea8cf-p182">Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können. In \<Befehlsargument\>-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p182">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. Within \<command-argument\> segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span>
  
### <a name="g-7-security-considerations"></a><span data-ttu-id="ea8cf-p183">G-7. Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p183">G-7. Security Considerations</span></span>

<span data-ttu-id="ea8cf-p184">Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-publisher-URIs bewirkt das Klicken auf einen Link zu einem ms-publisher-URI den Start der registrierten Anwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-publisher-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p184">On systems that have registered handlers to recognize and act on ms-publisher URIs, clicking on a link to an ms-publisher URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-publisher URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="g-9-references"></a><span data-ttu-id="ea8cf-p185">G-9. Referenzen</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p185">G-9. References</span></span>

<span data-ttu-id="ea8cf-425">RFC 3987 - International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="ea8cf-425">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-h---uri-scheme-registration-template-for-ms-spd-scheme"></a><span data-ttu-id="ea8cf-426">ANHANG H - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-SPD-SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ea8cf-426">APPENDIX H - URI SCHEME REGISTRATION TEMPLATE FOR MS-SPD SCHEME</span></span>
<span data-ttu-id="ea8cf-427"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="ea8cf-427"></span></span>

### <a name="h-3-uri-scheme-syntax"></a><span data-ttu-id="ea8cf-p186">H-3. URI-Schemasyntax</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p186">H-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="ea8cf-430">SharePoint Designer-Schema = „ms-spd:" open-for-edit-cmd</span><span class="sxs-lookup"><span data-stu-id="ea8cf-430">SharePoint Designer Scheme = "ms-spd:" open-for-edit-cmd</span></span>
    
> <span data-ttu-id="ea8cf-431">open-for-edit-cmd = „ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-431">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="ea8cf-432">document-uri = URI-Speicherort des zu öffnenden Dokuments</span><span class="sxs-lookup"><span data-stu-id="ea8cf-432">document-uri = URI location of document to open</span></span>
    
### <a name="h-4-uri-scheme-semantics"></a><span data-ttu-id="ea8cf-p187">H-4. URI-Schemasemantik</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p187">H-4. URI Scheme Semantics</span></span>

<span data-ttu-id="ea8cf-p188">Das Schema „ms-spd" definiert eine URI-Syntax zum Öffnen eines Microsoft SharePoint Designer-Dokuments. Das Schema definiert zwei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der SharePoint Designer anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, und (2) open-for-view-cmd (ofv), der SharePoint Designer anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p188">The ms-spd scheme defines a URI syntax for opening a Microsoft SharePoint Designer document. The scheme defines two commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs SharePoint Designer to open the document at the specified URI for editing; and 2) open-for-view-cmd (ofv), which instructs SharePoint Designer to open the document at the specified URI in a read-only mode.</span></span>
  
### <a name="h-5-applicationsprotocols-that-use-the-ms-spd-uri-scheme"></a><span data-ttu-id="ea8cf-p189">H-5. Anwendungen/Protokolle, die das URI-Schema „ms-spd" verwenden</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p189">H-5. Applications/Protocols that use the ms-spd URI Scheme</span></span>

<span data-ttu-id="ea8cf-p190">Das URI-Schema „ms-spd" wird von Microsoft Office 2013 zum Aufrufen von Microsoft SharePoint Designer 2013 von Webseiten aus verwendet. Microsoft SharePoint 2013 verwendet ms-spd-URIs als Links zu SharePoint Designer-Dokumenten in SharePoint-Dokumentbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p190">The ms-spd URI Scheme is used by Microsoft Office 2013 to invoke Microsoft SharePoint Designer 2013 from web pages. Microsoft SharePoint 2013 uses ms-spd URIs as links to SharePoint Designer documents stored in SharePoint document libraries.</span></span>
  
### <a name="h-6-interoperability-considerations"></a><span data-ttu-id="ea8cf-p191">H-6. Überlegungen zur Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p191">H-6. Interoperability Considerations</span></span>

<span data-ttu-id="ea8cf-p192">Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p192">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="ea8cf-446">In < *Befehlsargument*  >-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-446">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="h-7-security-considerations"></a><span data-ttu-id="ea8cf-p193">H-7. Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p193">H-7. Security Considerations</span></span>

<span data-ttu-id="ea8cf-p194">Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-spd-URIs bewirkt das Klicken auf einen Link zu einem ms-spd-URI den Start der registrierten Anwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-spd-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p194">On systems that have registered handlers to recognize and act on ms-spd URIs, clicking on a link to an ms-spd URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-spd URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="h-8-references"></a><span data-ttu-id="ea8cf-p195">H-8. Referenzen</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p195">H-8. References</span></span>

<span data-ttu-id="ea8cf-453">RFC 3987 - International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="ea8cf-453">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-i---uri-scheme-registration-template-for-ms-infopath-scheme"></a><span data-ttu-id="ea8cf-454">ANHANG I - URI-SCHEMAREGISTRIERUNGSVORLAGE FÜR DAS MS-INFOPATH-SCHEMA</span><span class="sxs-lookup"><span data-stu-id="ea8cf-454">APPENDIX I - URI SCHEME REGISTRATION TEMPLATE FOR MS-INFOPATH SCHEME</span></span>
<span data-ttu-id="ea8cf-455"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="ea8cf-455"></span></span>

###   <a name="i-3-uri-scheme-syntax"></a><span data-ttu-id="ea8cf-p196">I-3. URI-Schemasyntax</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p196">I-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="ea8cf-458">Infopath-Schema = „ms-infopath:" open-for-edit-cmd | open-for-view-cmd</span><span class="sxs-lookup"><span data-stu-id="ea8cf-458">Infopath Scheme = "ms-infopath:" open-for-edit-cmd | open-for-view-cmd</span></span>
    
> <span data-ttu-id="ea8cf-459">open-for-edit-cmd = „ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-459">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="ea8cf-460">open-for-view-cmd = „ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="ea8cf-460">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="ea8cf-461">document-uri = URI-Speicherort des zu öffnenden Dokuments</span><span class="sxs-lookup"><span data-stu-id="ea8cf-461">document-uri = URI location of document to open</span></span>
    
### <a name="i-4-uri-scheme-semantics"></a><span data-ttu-id="ea8cf-p197">I-4. URI-Schemasemantik</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p197">I-4. URI Scheme Semantics</span></span>

<span data-ttu-id="ea8cf-p198">Das Schema „ms-infopath" definiert eine URI-Syntax zum Öffnen oder Erstellen eines Microsoft Infopath-Dokuments. Das Schema definiert zwei Befehle, die als Anweisungen dafür dienen, was mit dem referenzierten Dokument geschehen soll. Die Befehle sind 1) open-for-edit-cmd (ofe), der Infopath anweist, das Dokument am angegebenen URI für die Bearbeitung zu öffnen, und (2) open-for-view-cmd (ofv), der Infopath anweist, das Dokument am angegebenen URI im schreibgeschützten Modus zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p198">The ms-infopath scheme defines a URI syntax for opening or creating a Microsoft Infopath document. The scheme defines two commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Visio to open the document at the specified URI for editing; and 2) open-for-view-cmd (ofv), which instructs Visio to open the document at the specified URI in a read-only mode.</span></span>
  
### <a name="i-5-applicationsprotocols-that-use-the-ms-infopath-uri-scheme"></a><span data-ttu-id="ea8cf-p199">I-5. Anwendungen/Protokolle, die das URI-Schema „ms-infopath" verwenden</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p199">I-5. Applications/Protocols that use the ms-infopath URI Scheme</span></span>

<span data-ttu-id="ea8cf-p200">Das URI-Schema „ms-infopath" wird von Microsoft Office 2013 zum Aufrufen von Microsoft Infopath 2013 von Webseiten aus verwendet. Microsoft SharePoint 2013 verwendet ms-infopath-URIs als Links zu Infopath-Dokumenten in SharePoint-Dokumentbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p200">The ms-infopath URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Infopath 2013 from web pages. Microsoft SharePoint 2013 uses ms-infopath URIs as links to Infopath documents stored in SharePoint document libraries.</span></span>
  
### <a name="i-6-interoperability-considerations"></a><span data-ttu-id="ea8cf-p201">I-6. Überlegungen zur Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p201">I-6. Interoperability Considerations</span></span>

<span data-ttu-id="ea8cf-p202">Beachten Sie, dass der senkrechte Strich, der in dieser Spezifikation als Trennzeichen verwendet wird, nicht unter den im Abschnitt 2.2 von RFC 3986 zur potenziellen Verwendung als Trennzeichen reservierten Zeichen genannt ist. Dies geschieht absichtlich, um die Menge der Zeichen zu maximieren, die ohne Codierung mit Prozentzeichen im URI-Befehlsargument verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p202">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="ea8cf-475">In < *Befehlsargument*  >-Segmenten sind die in RFC 3986 reservierten Zeichen „:" und „/" Teil der Argumentdaten und keine Trennzeichen und werden daher ohne Escapezeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-475">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="i-7-security-considerations"></a><span data-ttu-id="ea8cf-p203">I-7. Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p203">I-7. Security Considerations</span></span>

<span data-ttu-id="ea8cf-p204">Auf Systemen mit registrierten Handlern zum Erkennen und Verarbeiten von ms-infopath-URIs bewirkt das Klicken auf einen Link zu einem ms-infopath-URI den Start der registrierten Anwendung. Dabei werden an die Anwendung Anweisungen zum Öffnen eines Dokuments am angegebenen URI übergeben. Anwendungen, die zur Verarbeitung von ms-infopath-URIs registriert werden, sollten Schutzmaßnahmen gegen das Öffnen von Dokumenten von nicht vertrauenswürdigen Remotesystemen implementieren, die bösartigen Code enthalten können.</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p204">On systems that have registered handlers to recognize and act on ms-infopath URIs, clicking on a link to an ms-infopath URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-infopath URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="i-8-references"></a><span data-ttu-id="ea8cf-p205">I-8. Referenzen</span><span class="sxs-lookup"><span data-stu-id="ea8cf-p205">I-8. References</span></span>

<span data-ttu-id="ea8cf-482">RFC 3987 - International Resource Identifiers (IRIs)</span><span class="sxs-lookup"><span data-stu-id="ea8cf-482">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  

