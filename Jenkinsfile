node {
    stage 'configure'
        def archiveUrl = 'http://opendata.eol.org/dataset/3fefcaf0-79aa-44f3-8ffc-74ba7029de73/resource/a56647f9-f438-413e-b54a-b44fae7e14b2/download/emammal.zip'

    stage 'import'
        sh "wget --quiet https://raw.githubusercontent.com/gimmefreshdata/archive-importer/master/archives.groovy -O archives.groovy"
        archives = load 'archives.groovy'
        archives.importIfChanged(archiveUrl)
}
