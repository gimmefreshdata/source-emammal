node {
    stage 'configure'
        def archiveUrl = 'http://opendata.eol.org/dataset/e96c8aca-7100-4ddd-b2c7-bdad1830f96a/resource/91b6fd56-1506-4ace-879c-1965bcfc93c5/download/emammal.zip'

    stage 'import'
        sh "wget --quiet https://raw.githubusercontent.com/gimmefreshdata/archive-importer/master/archives.groovy -O archives.groovy"
        archives = load 'archives.groovy'
        archives.importIfChanged(archiveUrl)
}
