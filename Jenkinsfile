node {
    stage 'configure'
        def archiveUrl = 'https://editors.eol.org/eol_php_code/applications/content_server/resources/eMammal.zip'

    stage 'import'
        sh "wget --quiet https://raw.githubusercontent.com/gimmefreshdata/archive-importer/master/archives.groovy -O archives.groovy"
        archives = load 'archives.groovy'
        archives.importIfChanged(archiveUrl)
}
